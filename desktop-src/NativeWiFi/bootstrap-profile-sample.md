---
description: Usado para autenticar em uma rede sem fio pela primeira vez antes que o computador ingresse em um domínio.
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: Exemplo de perfil Bootstrap
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96c7daa6bdc72146400973d08c9e5780092b214a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170040"
---
# <a name="bootstrap-profile-sample"></a><span data-ttu-id="f42c9-103">Exemplo de perfil Bootstrap</span><span class="sxs-lookup"><span data-stu-id="f42c9-103">Bootstrap Profile Sample</span></span>

<span data-ttu-id="f42c9-104">O exemplo de perfil de Bootstrap pode ser usado para autenticar em uma rede sem fio pela primeira vez antes que o computador ingresse em um domínio.</span><span class="sxs-lookup"><span data-stu-id="f42c9-104">The Bootstrap profile sample can be used to authenticate to a wireless network for the first time before the computer has joined a domain.</span></span>

<span data-ttu-id="f42c9-105">Esse perfil não valida os certificados apresentados pelo servidor de serviço RADIUS (RADIUS) e não deve ser usado depois que o computador é ingressado em um domínio.</span><span class="sxs-lookup"><span data-stu-id="f42c9-105">This profile does not validate the certificates presented by the Remote Authentication Dial-In User Service (RADIUS) server, and should not be used after the machine is joined to a domain.</span></span>

<span data-ttu-id="f42c9-106">Este exemplo é configurado para usar a segurança do Wi-Fi Protected Access 2 em execução no modo empresarial (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="f42c9-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="f42c9-107">Outros tipos de segurança podem ser usados contanto que o método de autenticação seja PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="f42c9-107">Other security types can be used as long as the authentication method is PEAP-MSCHAPv2.</span></span>

<span data-ttu-id="f42c9-108">**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="f42c9-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="f42c9-109">A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f42c9-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="f42c9-110">A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="f42c9-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="f42c9-111">A configuração padrão era "true" no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f42c9-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="f42c9-112">Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f42c9-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="f42c9-113">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f42c9-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="f42c9-114">O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f42c9-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="f42c9-115">Os filhos [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**AuthMode**](onexschema-authmode-onex-element.md)e [**logon único**](onexschema-singlesignon-onex-element.md) do elemento [**Onex**](onexschema-onex-element.md) não têm suporte e devem ser removidos do perfil antes do uso.</span><span class="sxs-lookup"><span data-stu-id="f42c9-115">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
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
                <authMode>machineOrUser</authMode>
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
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="f42c9-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f42c9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f42c9-117">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="f42c9-117">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="f42c9-118">Unindo um cliente sem fio do Windows Vista a um domínio</span><span class="sxs-lookup"><span data-stu-id="f42c9-118">Joining a Windows Vista Wireless Client to a Domain</span></span>](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



