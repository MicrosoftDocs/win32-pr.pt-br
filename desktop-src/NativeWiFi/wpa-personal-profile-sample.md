---
description: Usa uma chave pré-compartilhada para autenticação de rede.
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Exemplo de perfil de WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4a69fffcb0432e420121ed76c76889eb8bb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760228"
---
# <a name="wpa-personal-profile-sample"></a>Exemplo de perfil de WPA-Personal

Este perfil de exemplo usa uma chave pré-compartilhada para autenticação de rede. A chave é compartilhada com o cliente e o ponto de acesso. Este perfil de exemplo está configurado para usar Wi-Fi segurança de acesso protegido em execução no modo pessoal (WPA-Personal). O TKIP (Temporal Key Integrity Protocol) é usado para criptografia.

**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado. A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e no Windows Vista. Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

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

A chave compartilhada foi omitida deste perfil de exemplo. Se você tentar usar este perfil de exemplo para se conectar a uma rede, será solicitado que você insira uma chave compartilhada. Você pode evitar esse prompt adicionando um elemento filho [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) ao elemento [**Security**](wlan-profileschema-security-msm-element.md) imediatamente após o elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

O trecho a seguir mostra um elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contém uma chave não criptografada. Você deve substituir o comentário `<!-- insert key here -->` pela chave não criptografada real antes de usar esse trecho de código em um perfil.

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

 

 



