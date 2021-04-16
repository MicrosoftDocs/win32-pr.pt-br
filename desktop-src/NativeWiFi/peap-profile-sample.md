---
description: Usado para se conectar a uma rede que usa o protocolo de autenticação extensível protegido com o protocolo PEAP-MSCHAPv2 da Microsoft, com o nome de usuário/senha para autenticação 802.1 X.
ms.assetid: b5dde0d0-940f-40ec-b24d-95a76325ff1b
title: Exemplo de perfil de PEAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db34a3a99305f3506e3b34fde48f41e5a4c72ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758600"
---
# <a name="peap-profile-sample"></a><span data-ttu-id="a7996-103">Exemplo de perfil de PEAP</span><span class="sxs-lookup"><span data-stu-id="a7996-103">PEAP Profile Sample</span></span>

<span data-ttu-id="a7996-104">Este exemplo de perfil mostra um perfil de rede com fio usado para se conectar a uma rede que usa o protocolo de autenticação extensível protegida com o protocolo PEAP-MSCHAPv2 da Microsoft, com \* UserName \*, **/** _senha_ para autenticação 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="a7996-104">This profile sample shows a wired network profile used to connect to a network that uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ for 802.1X authentication.</span></span> <span data-ttu-id="a7996-105">O usuário é solicitado a inserir as credenciais.</span><span class="sxs-lookup"><span data-stu-id="a7996-105">The user is prompted to enter credentials.</span></span>

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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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
</LANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="a7996-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7996-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7996-107">Exemplos de perfil com fio</span><span class="sxs-lookup"><span data-stu-id="a7996-107">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 



