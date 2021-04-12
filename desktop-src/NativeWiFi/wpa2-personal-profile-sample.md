---
description: Usa uma chave pré-compartilhada para autenticação de rede.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Exemplo de perfil de WPA2-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0054bc28962113a85bb909d4e8cd173b3bc16974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297273"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="ddcb5-103">Exemplo de perfil de WPA2-Personal</span><span class="sxs-lookup"><span data-stu-id="ddcb5-103">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="ddcb5-104">Este perfil de exemplo usa uma chave pré-compartilhada para autenticação de rede.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-104">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="ddcb5-105">A chave é compartilhada com o cliente e o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-105">The key is shared with the client and the access point.</span></span> <span data-ttu-id="ddcb5-106">Este perfil de exemplo está configurado para usar a segurança do Wi-Fi Protected Access 2 em execução no modo pessoal (WPA2-Pessoal).</span><span class="sxs-lookup"><span data-stu-id="ddcb5-106">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="ddcb5-107">O tipo de codificação criptografia AES (AES) é usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="ddcb5-108">**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="ddcb5-109">A configuração padrão para [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando este elemento não está definido em um perfil de LAN sem fio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="ddcb5-110">A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="ddcb5-111">A configuração padrão era "true" no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="ddcb5-112">Veja a descrição do elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="ddcb5-113">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O [**nome**](wlan-profileschema-name-wlanprofile-element.md) filho do elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="ddcb5-114">O nome do perfil, conforme armazenado no repositório de perfis, é derivado do [**nome**](wlan-profileschema-name-ssid-element.md) filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ddcb5-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="ddcb5-115">A chave compartilhada foi omitida deste perfil de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-115">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="ddcb5-116">Se você tentar usar este perfil de exemplo para se conectar a uma rede, será solicitado que você insira uma chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-116">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="ddcb5-117">Você pode evitar esse prompt adicionando um elemento filho [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) ao elemento [**Security**](wlan-profileschema-security-msm-element.md) imediatamente após o elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ddcb5-117">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="ddcb5-118">O trecho a seguir mostra um elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contém uma chave não criptografada.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-118">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="ddcb5-119">Você deve substituir o comentário `<!-- insert key here -->` pela chave não criptografada real antes de usar esse trecho de código em um perfil.</span><span class="sxs-lookup"><span data-stu-id="ddcb5-119">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="ddcb5-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddcb5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddcb5-121">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="ddcb5-121">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



