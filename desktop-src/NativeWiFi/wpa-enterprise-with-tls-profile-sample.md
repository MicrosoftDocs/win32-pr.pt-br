---
description: Usa eAP-TLS (Segurança de Nível de Transporte do Protocolo de Autenticação Extensível) com certificados para autenticar na rede (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise exemplo de perfil TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ebb9fa779c1a1d9a4e77c20d462f31fcafc9ec562e47ae106386b58c112a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619033"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>WPA-Enterprise exemplo de perfil TLS

Este perfil de exemplo usa eAP-TLS (Segurança de Nível de Transporte do Protocolo de Autenticação Extensível) com certificados para autenticação na rede.

Este exemplo está configurado para usar Wi-Fi segurança de Acesso Protegido em execução no modo Enterprise (WPA-Enterprise). O WPA-Enterprise de segurança usa 802.1X para a troca de autenticação com o back-end. O protocolo TKIP é usado para criptografia.

As credenciais EAP-TLS são obtidas do armazenamento de certificados. Se a autenticação com base nas credenciais no armazenamento de certificados falhar, o usuário será solicitado a fornecer credenciais válidas. Nenhum servidor alternativo, autoridades de certificação raiz ou nomes de usuário serão usados para autenticação se a primeira tentativa falhar.

A configuração de EAPHost usada neste exemplo de perfil sem fio foi derivada do exemplo propriedades de conexão [EAP-TLS.](../eaphost/eap-tls-connection-properties.md)

**Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado:** As alterações são implementadas no Windows 7 e Windows Server 2008 R2 com o Serviço de LAN Sem Fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão [**para autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando esse elemento não está definido em um perfil de LAN sem fio foi alterada. A configuração padrão é alterada para "false" no Windows 7 e Windows Server 2008 R2 com o Serviço lan sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e Windows Vista. Consulte a descrição [**do elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para EAP-TLS.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
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

 

 
