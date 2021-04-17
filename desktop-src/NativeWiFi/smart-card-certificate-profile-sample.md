---
description: Usado para se conectar a uma rede que usa certificados EAP-TLS (Extensible Authentication Protocol Transport Level Security) armazenados em um cartão inteligente para autenticação 802.1 X.
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: Exemplo de perfil de certificado de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13373ea66a7ed93ad527715de9f32d4f72705be5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758599"
---
# <a name="smart-card-certificate-profile-sample"></a>Exemplo de perfil de certificado de cartão inteligente

Este exemplo de perfil mostra um perfil de rede com fio usado para se conectar a uma rede que usa certificados EAP-TLS (Extensible Authentication Protocol Transport Level Security) armazenados em um cartão inteligente para autenticação 802.1 X. Para ver um perfil que usa certificados EAP-TLS armazenados no computador local, consulte [exemplo de perfil de certificado do computador](machine-certificate-profile-sample.md).

A configuração EAPHost usada neste exemplo de perfil sem fio foi derivada da amostra de [Propriedades de conexão EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
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
                                        <eapTls:SmartCard />
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
</LANProfile>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de perfil com fio](wired-profile-samples.md)
</dt> </dl>

 

 
