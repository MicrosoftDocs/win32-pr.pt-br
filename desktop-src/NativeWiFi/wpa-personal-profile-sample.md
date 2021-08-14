---
description: Usa uma chave pré-compartilhada para autenticação de rede. Este perfil de exemplo usa Wi-Fi segurança de Acesso Protegido em execução no modo Pessoal (WPA-Personal).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: exemplo WPA-Personal perfil do WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d196a327672ae31cb52d275be79193860fd89fff29f169be63018f5b848a4268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797416"
---
# <a name="wpa-personal-profile-sample"></a>exemplo WPA-Personal perfil do WPA-Personal

Este perfil de exemplo usa uma chave pré-compartilhada para autenticação de rede. A chave é compartilhada com o cliente e o ponto de acesso. Este perfil de exemplo está configurado para usar Wi-Fi segurança de Acesso Protegido em execução no modo Pessoal (WPA-Personal). O protocolo TKIP é usado para criptografia.

**Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado:** As alterações são implementadas no Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão [**para autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando esse elemento não está definido em um perfil de LAN sem fio foi alterada. A configuração padrão é alterada para "false" no Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e Windows Vista. Consulte a descrição [**do elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do [**elemento WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no armazenamento de perfil, é derivado do nome [**filho**](wlan-profileschema-name-ssid-element.md) do [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

A chave compartilhada foi omitida deste perfil de exemplo. Se você tentar usar esse perfil de exemplo para se conectar a uma rede, será solicitado que você insira uma chave compartilhada. Você pode evitar esse prompt adicionando um [**elemento filho sharedKey**](wlan-profileschema-sharedkey-security-element.md) ao elemento [**de**](wlan-profileschema-security-msm-element.md) segurança imediatamente após o [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

O snippet a seguir mostra [**um elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contém uma chave não criptografada. Você deve substituir o comentário `<!-- insert key here -->` pela chave não criptografada real antes de usar esse snippet em um perfil.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> </dl>

 

 



