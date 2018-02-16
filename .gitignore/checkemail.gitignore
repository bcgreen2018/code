<!-- РќР°С‡Р°Р»Рѕ СЃРєСЂРёРїС‚Р° РѕР±СЂР°Р±РѕС‚РєРё email РїРѕР»СЏ -->
$('[data-type="email"] input').change(function() {
    var i,j;
// РџРѕР»СѓС‡Р°РµРј Р·РЅР°С‡РµРЅРёРµ РїРѕР»СЏ email
    var emailtext = $(this).val();
// РЈРґР°Р»СЏРµРј РїСЂРѕР±РµР»С‹
    var email = emailtext.replace(/\s/g, '');
// РЈРґР°Р»СЏРµРј Р»РёС€РЅРёРµ СЃРёРјРІРѕР»С‹
    email = email.replace(/\//g, '');
// РЈРґР°Р»СЏРµРј/Р·Р°РјРµРЅСЏРµРј СЂСѓСЃСЃРєРёРµ Р±СѓРєРІС‹
    var rualphabet = new Array({'Рђ' : 'a'},{'Р°' : 'a'},{'Р‘' : ''},{'Р±' : ''},{'Р’' : 'b'},{'РІ' : 'b'},{'Р“' : ''},{'Рі' : ''},{'Р”' : ''},{'Рґ' : ''},{'Р•' : 'e'},{'Рµ' : 'e'},{'РЃ' : 'e'},{'С‘' : 'e'},{'Р–' : ''},{'Р¶' : ''},{'Р—' : ''},{'Р·' : ''},{'Р' : ''},{'Рё' : ''},{'Р™' : ''},{'Р№' : ''},{'Рљ' : 'k'},{'Рє' : 'k'},{'Р›' : ''},{'Р»' : ''},{'Рњ' : 'm'},{'Рј' : 'm'},{'Рќ' : 'h'},{'РЅ' : 'h'},{'Рћ' : 'o'},{'Рѕ' : 'o'},{'Рџ' : ''},{'Рї' : ''},{'Р ' : 'p'},{'СЂ' : 'p'},{'РЎ' : 'c'},{'СЃ' : 'c'},{'Рў' : 't'},{'С‚' : 't'},{'РЈ' : 'y'},{'Сѓ' : 'y'},{'Р¤' : ''},{'С„' : ''},{'РҐ' : 'x'},{'С…' : 'x'},{'Р¦' : ''},{'С†' : ''},{'Р§' : ''},{'С‡' : ''},{'Р©' : ''},{'С‰' : ''},{'РЁ' : ''},{'С€' : ''},{'РЄ' : ''},{'СЉ' : ''},{'Р«' : ''},{'С‹' : ''},{'Р¬' : ''},{'СЊ' : ''},{'Р­' : ''},{'СЌ' : ''},{'Р®' : ''},{'СЋ' : ''},{'РЇ' : ''},{'СЏ' : ''});
    for(i=0; i < rualphabet.length; i++) {
        var regEx = new RegExp(Object.keys(rualphabet[i])[0], "g");
        email = email.replace(regEx, rualphabet[i][Object.keys(rualphabet[i])[0]]);
    }
// РџСЂРѕРІРµСЂСЏРµРј РЅР° РїСЂР°РІРёР»СЊРЅРѕРµ РѕРєРѕРЅС‡Р°РЅРёРµ РїРѕС‡С‚РѕРІРѕР№ СЃРёСЃС‚РµРјС‹
    var emailParts = email.split('@');
    if(emailParts.length == 2 && emailParts[1].length > 0) {
        emailParts[1] = emailParts[1].replace(/[^0-9a-zA-Z.*]/g, "");
        var emailPlatforms = [{'mail.ru' : [
                'mai.ru',
                'mai.ri',
                'mai.ru',
                'mali.ru',
                'mail.ry',
                'mail.li',
                'vail.ru',
                'mail.',
                'maail.ru',
                'maii.ru',
                'mail..ru',
                'mail..ua',
                'mail.com',
                'mail.r',
                'mail.ku',
                'mail.fu',
                'mal.ru',
                'majl.ru',
                'maul.ru',
                'mail.u',
                'mil.ru',
                '.mail.ru',
                'mail.ru.',
                'mail.xn--c1an'
            ]},
            {'yandex.ru' : [
                'ayndex.ru',
                'yande.ru',
                'yadnex.ru',
                'yadex.ru',
                'yandex.ry',
                'yandex.ri',
                'andex.ru',
                'eandex.ru',
                'yandex.',
                'jandex.ru',
                'tandex.ru',
                'uandex.ru',
                'yandx.ru',
                'yndex.ru',
                'yandeks.ru',
                'yndeks.ru',
                'yanex.ru',
                'yandex.u',
                'yandex.r',
                '.yandex.ru',
                'yandex.ru.'
            ]},
            {'gmail.com' : [
                'gamil.com',
                'gmial.com',
                'gmai.com',
                'google.ru',
                'google.com',
                'gmail.ru',
                'gmail.ry',
                'gmail.ri',
                'cmail.com',
                'ggmail.com',
                'gmaik.com',
                'gmail.c',
                'gmail.co',
                'gmail.cm',
                'gmail.kom',
                'gmail.cmp',
                'gmail.cov',
                'gmail.con',
                'gmail.',
                'gmil.com',
                'gmal.com',
                'gnail.com',
                'googlemail.com',
                'gvail.com',
                'gmailc.com',
                'jmail.com',
                'qmail.com',
                '.gmail.com',
                'gmail.com.'
            ]},
            {'list.ru' : [
                'ilst.ru',
                'lits.ru',
                'lis.tru',
                'list.ry',
                'list.ri',
                'ist.ru',
                'list.',
                'lirt.ru',
                'lisn.ru',
                'lisr.ru',
                'list.u',
                'list.r',
                '.list.ru',
                'list.ru.'
            ]},
            {'bk.ru' : [
                'kb.ru',
                'bk.ry',
                'bk.ri',
                'bkk.ru',
                'bk.',
                'bk.u',
                'bk.r',
                '.bk.ru',
                'bk.ru.'
            ]},
            {'yahoo.com' : [
                'ayhoo.com',
                'yahoo.ru',
                'yaho.com',
                'yahoo.',
                '.yahoo.com',
                'yahoo.com.'
            ]},
            {'hotmail.com' : [
                'hotmail.',
                '.hotmail.com',
                'hotmail.com.'
            ]},
            {'rambler.ru' : [
                'rambler.ry',
                'rambler.ru',
                'rambler.com',
                'rable.ru',
                'ambler.ru',
                'rambler.',
                'ramber.ru',
                'rambker.ru',
                'rabler.ru',
                'ramble.ru',
                'ramblere.ru',
                'rambller.ru',
                'rambltr.ru',
                'ramdler.ru',
                'tabler.ru',
                'rambler.u',
                'rambler.r',
                '.rambler.ru',
                'rambler.ru.'
            ]},
            {'inbox.ru' : [
                'ibnox.ru',
                'inbox.com',
                'inbo.ru',
                'inbox.u',
                'inbox.r',
                '.inbox.ru',
                'inbox.ru.'
            ]}];
        var trueDomain,
            failDomain;
        for(i=0; i < emailPlatforms.length; i++) {
            trueDomain = Object.keys(emailPlatforms[i])[0];
            for(j=0; j < emailPlatforms[i][trueDomain].length; j++) {
                failDomain = emailPlatforms[i][trueDomain][j];

                if(emailParts[1] == failDomain)
                    emailParts[1] = emailParts[1].replace(failDomain, trueDomain);
                if(emailParts[1] == "." + failDomain)
                    emailParts[1] = emailParts[1].replace("." + failDomain, trueDomain);
                if(emailParts[1] == failDomain + ".")
                    emailParts[1] = emailParts[1].replace(failDomain + ".", trueDomain);
            }
        }
        email = emailParts[0] + "@" + emailParts[1];
    }

// РЎРѕС…СЂР°РЅСЏРµРј РѕР±СЂР°Р±РѕС‚Р°РЅРЅРѕРµ Р·РЅР°С‡РµРЅРёРµ
    $(this).val(email);
});
<!-- РљРѕРЅРµС† СЃРєСЂРёРїС‚Р° РѕР±СЂР°Р±РѕС‚РєРё email РїРѕР»СЏ -->
