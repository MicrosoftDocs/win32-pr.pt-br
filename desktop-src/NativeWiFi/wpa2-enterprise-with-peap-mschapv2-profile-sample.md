---
description: Usa o protocolo de autenticação extensível protegida com o protocolo de autenticação de handshake de desafio da Microsoft versão 2 (PEAP-MSCHAPv2) com nome de usuário/senha para autenticar na rede.
ms.assetid: fcbc74a6-1990-45a0-af2e-1c343a84497a
title: WPA2-Enterprise com PEAP-MSCHAPv2 exemplo de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43363be10a6d7d77d445e188b1c3084f71ce3b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757763"
---
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="eb81c-103">WPA2-Enterprise com PEAP-MSCHAPv2 exemplo de perfil</span><span class="sxs-lookup"><span data-stu-id="eb81c-103">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="eb81c-104">Este perfil de exemplo usa o protocolo de autenticação extensível protegida com o protocolo PEAP-MSCHAPv2 da Microsoft, com a senha \* UserName \* **/**  para autenticar-se na rede.</span><span class="sxs-lookup"><span data-stu-id="eb81c-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="eb81c-105">O usuário é solicitado a inserir as credenciais.</span><span class="sxs-lookup"><span data-stu-id="eb81c-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="eb81c-106">Este exemplo é configurado para usar a segurança do Wi-Fi Protected Access 2 em execução no modo empresarial (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="eb81c-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="eb81c-107">O tipo de segurança WPA2-Enterprise usa 802.1 X para a troca de autenticação com o back-end.</span><span class="sxs-lookup"><span data-stu-id="eb81c-107">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="eb81c-108">O tipo de codificação criptografia AES (AES) é usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="eb81c-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="eb81c-109">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="eb81c-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="eb81c-110">O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eb81c-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
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
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="eb81c-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb81c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb81c-112">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="eb81c-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



