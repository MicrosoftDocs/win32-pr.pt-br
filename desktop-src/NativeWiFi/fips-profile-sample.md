---
description: Usado para se conectar a uma rede que requer configurações de segurança que estão em conformidade com o padrão FIPS 140-2.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: Exemplo de perfil FIPS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6d24f82a815c752a662af5f093dd9a7c34de33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091714"
---
# <a name="fips-profile-sample"></a><span data-ttu-id="e6f0e-103">Exemplo de perfil FIPS</span><span class="sxs-lookup"><span data-stu-id="e6f0e-103">FIPS Profile Sample</span></span>

<span data-ttu-id="e6f0e-104">O exemplo de perfil FIPS pode ser usado para se conectar a uma rede que exige configurações de segurança que estejam de acordo com o padrão FIPS 140-2 (Federal Information Processing Standards).</span><span class="sxs-lookup"><span data-stu-id="e6f0e-104">The FIPS profile sample can be used to connect to a network that requires security settings that comply with Federal Information Processing Standards (FIPS) 140-2 standard.</span></span> <span data-ttu-id="e6f0e-105">Para obter mais informações sobre o FIPS, consulte [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md).</span><span class="sxs-lookup"><span data-stu-id="e6f0e-105">For more information about FIPS, see [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).</span></span>

<span data-ttu-id="e6f0e-106">**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-106">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="e6f0e-107">A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-107">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="e6f0e-108">A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-108">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="e6f0e-109">A configuração padrão era "true" no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-109">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="e6f0e-110">Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-110">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="e6f0e-111">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e6f0e-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="e6f0e-112">O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f0e-112">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="e6f0e-113">Não há suporte para o elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f0e-113">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>FIPS_TEST</name>
    <SSIDConfig>
        <SSID>
            <hex>464950535F54455354</hex>
            <name>FIPS_TEST</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
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
                <FIPSMode xmlns="https://www.microsoft.com/networking/WLAN/profile/v2">true</FIPSMode>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig">
                    <EapMethod>
                        <Type xmlns="https://www.microsoft.com/provisioning/EapCommon">25</Type>
                        <VendorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                        <VendorType xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                        <AuthorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                    </EapMethod>
                    <ConfigBlob></ConfigBlob>
                    </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="e6f0e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6f0e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6f0e-115">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="e6f0e-115">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



