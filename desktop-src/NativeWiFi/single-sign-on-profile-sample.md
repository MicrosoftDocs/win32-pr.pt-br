---
description: Usado para cenários que exigem autenticação 802.1X antes Windows logon.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Exemplo Sign-On perfil de usuário único
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f89f7e9c39123cd7bf55c8bc48ff69d007d150c086714c82c37619c477dd25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797947"
---
# <a name="single-sign-on-profile-sample"></a>Exemplo Sign-On perfil de usuário único

O exemplo de perfil de SSO (logon único) pode ser usado para cenários que exigem autenticação 802.1X antes Windows logon.

Este exemplo está configurado para usar Wi-Fi segurança do Acesso Protegido 2 em execução no modo Enterprise (WPA2-Enterprise). O Protocolo de Autenticação Extensível Protegido com o Protocolo de Autenticação de Handshake do Microsoft Challenge versão 2 (PEAP-MSCHAPv2) é usado para autenticação de rede. As Windows de logon do usuário são usadas para PEAP-MSCHAPv2 autenticação.

Embora este exemplo seja configurado para usar WPA2-Enterprise e PEAP-MSCHAPv2, os perfis de SSO podem ser configurados com outros tipos de segurança e autenticação.

**Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado:** As alterações são implementadas no Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão [**para autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando esse elemento não está definido em um perfil de LAN sem fio foi alterada. A configuração padrão é alterada para "false" no Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e Windows Vista. Consulte a descrição [**do elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do [**elemento WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no armazenamento de perfil, é derivado do nome [**filho**](wlan-profileschema-name-ssid-element.md) do [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md) Os [**filhos cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures,**](onexschema-maxauthfailures-onex-element.md) [**authMode**](onexschema-authmode-onex-element.md)e [**singleSignOn**](onexschema-singlesignon-onex-element.md) do [**elemento OneX**](onexschema-onex-element.md) não têm suporte e devem ser removidos do perfil antes do uso.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de perfil sem fio](wireless-profile-samples.md)
</dt> </dl>

 

 



