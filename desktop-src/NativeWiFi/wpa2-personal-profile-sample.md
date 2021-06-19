---
description: Usa uma chave pré-compartilhada para autenticação de rede. Este perfil de exemplo usa Wi-Fi segurança do Acesso Protegido 2 em execução no modo Pessoal (WPA2-Personal).
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: exemplo WPA2-Personal perfil do WPA2-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394861"
---
# <a name="wpa2-personal-profile-sample"></a>exemplo WPA2-Personal perfil do WPA2-Personal

Este perfil de exemplo usa uma chave pré-compartilhada para autenticação de rede. A chave é compartilhada com o cliente e o ponto de acesso. Este perfil de exemplo está configurado para usar Wi-Fi segurança do Acesso Protegido 2 em execução no modo Pessoal (WPA2-Personal). O tipo de criptografia criptografia AES (AES) é usado para criptografia.

**Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o Serviço de LAN Sem Fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão para [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando esse elemento não está definido em um perfil de LAN sem fio foi alterada. A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o Serviço lan sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e no Windows Vista. Consulte a descrição [**do elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do [**elemento WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no armazenamento de perfil, é derivado do nome [**filho**](wlan-profileschema-name-ssid-element.md) do [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

A chave compartilhada foi omitida deste perfil de exemplo. Se você tentar usar esse perfil de exemplo para se conectar a uma rede, será solicitado que você insira uma chave compartilhada. Você pode evitar esse prompt adicionando um [**elemento filho sharedKey**](wlan-profileschema-sharedkey-security-element.md) ao elemento [**de**](wlan-profileschema-security-msm-element.md) segurança imediatamente após o [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

O snippet a seguir mostra um [**elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contém uma chave não criptografada. Você deve substituir o comentário `<!-- insert key here -->` pela chave não criptografada real antes de usar esse snippet em um perfil.

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

 

 



