---
description: Usa EAP-TLS (segurança de nível de transporte) do protocolo de autenticação extensível com certificados para autenticar na rede.
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise com exemplo de perfil TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922535"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>WPA-Enterprise com exemplo de perfil TLS

Este perfil de exemplo usa EAP-TLS (segurança de nível de transporte) do protocolo de autenticação extensível com certificados para autenticar na rede.

Este exemplo é configurado para usar Wi-Fi segurança de acesso protegido em execução no modo empresarial (WPA-Enterprise). O tipo de segurança WPA-Enterprise usa 802.1 X para a troca de autenticação com o back-end. O TKIP (Temporal Key Integrity Protocol) é usado para criptografia.

As credenciais EAP-TLS são obtidas do repositório de certificados. Se a autenticação com base nas credenciais no repositório de certificados falhar, o usuário receberá uma solicitação para fornecer credenciais válidas. Nenhum servidor alternativo, autoridades de certificação raiz ou nomes de usuário serão usados para autenticação se a primeira tentativa falhar.

A configuração EAPHost usada neste exemplo de perfil sem fio foi derivada da amostra de [Propriedades de conexão EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio. A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado. A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e no Windows Vista. Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.

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

 

 
