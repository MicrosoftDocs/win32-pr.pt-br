---
description: Usado para se conectar a redes que não difundem seu nome de rede ou SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Exemplo de perfil sem difusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775682"
---
# <a name="non-broadcast-profile-sample"></a>Exemplo de perfil sem difusão

O exemplo de perfil sem difusão pode ser usado para se conectar a redes que não difundem seu nome de rede ou SSID.

Este perfil de exemplo está configurado para usar Wi-Fi segurança de acesso protegido em execução no modo pessoal (WPA-Personal). O TKIP (Temporal Key Integrity Protocol) é usado para criptografia. Perfis que usam outros tipos de segurança e codificação também podem ser configurados como perfis sem difusão.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

 

 



