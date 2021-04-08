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
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="5ac9d-103">WPA-Enterprise com exemplo de perfil TLS</span><span class="sxs-lookup"><span data-stu-id="5ac9d-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="5ac9d-104">Este perfil de exemplo usa EAP-TLS (segurança de nível de transporte) do protocolo de autenticação extensível com certificados para autenticar na rede.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="5ac9d-105">Este exemplo é configurado para usar Wi-Fi segurança de acesso protegido em execução no modo empresarial (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="5ac9d-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="5ac9d-106">O tipo de segurança WPA-Enterprise usa 802.1 X para a troca de autenticação com o back-end.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="5ac9d-107">O TKIP (Temporal Key Integrity Protocol) é usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="5ac9d-108">As credenciais EAP-TLS são obtidas do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="5ac9d-109">Se a autenticação com base nas credenciais no repositório de certificados falhar, o usuário receberá uma solicitação para fornecer credenciais válidas.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="5ac9d-110">Nenhum servidor alternativo, autoridades de certificação raiz ou nomes de usuário serão usados para autenticação se a primeira tentativa falhar.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="5ac9d-111">A configuração EAPHost usada neste exemplo de perfil sem fio foi derivada da amostra de [Propriedades de conexão EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac9d-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="5ac9d-112">**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="5ac9d-113">A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="5ac9d-114">A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="5ac9d-115">A configuração padrão era "true" no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5ac9d-116">Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="5ac9d-117">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5ac9d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ac9d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ac9d-119">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="5ac9d-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
