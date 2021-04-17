---
description: Usado para cenários que exigem autenticação 802.1 X antes do logon do Windows.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Exemplo de perfil de Sign-On único
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 077ed95095150e81ad9a3d7412d1940dcb1b33e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782305"
---
# <a name="single-sign-on-profile-sample"></a>Exemplo de perfil de Sign-On único

O exemplo de perfil de SSO (logon único) pode ser usado para cenários que exigem autenticação 802.1 X antes do logon do Windows.

Este exemplo é configurado para usar a segurança do Wi-Fi Protected Access 2 em execução no modo empresarial (WPA2-Enterprise). O protocolo de autenticação extensível protegida com o protocolo PEAP-MSCHAPv2 da Microsoft é usado para autenticação de rede. As credenciais de logon do Windows são usadas para PEAP-MSCHAPv2 autenticação.

Embora este exemplo esteja configurado para usar WPA2-Enterprise e PEAP-MSCHAPv2, os perfis de SSO podem ser configurados com outros tipos de segurança e autenticação.

**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado. A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e no Windows Vista. Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado. O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) . Os filhos [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**AuthMode**](onexschema-authmode-onex-element.md)e [**logon único**](onexschema-singlesignon-onex-element.md) do elemento [**Onex**](onexschema-onex-element.md) não têm suporte e devem ser removidos do perfil antes do uso.

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

 

 



