---
description: Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2) dão suporte apenas a um subconjunto dos elementos descritos no \_ esquema do perfil WLAN e material de referência do esquema Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidade de perfis sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505923"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="91249-103">Compatibilidade de perfis sem fio</span><span class="sxs-lookup"><span data-stu-id="91249-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="91249-104">Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2) dão suporte apenas a um subconjunto dos elementos descritos no [ \_ esquema do perfil WLAN](wlan-profileschema-schema.md) e material de referência do [esquema Onex](onexschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="91249-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="91249-105">Todos os perfis que estão em conformidade com os requisitos do Windows XP com SP3 e da API de LAN sem fio para Windows XP com SP2 também podem ser usados no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="91249-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="91249-106">\_Suporte a perfis WLAN</span><span class="sxs-lookup"><span data-stu-id="91249-106">WLAN\_profile Support</span></span>

<span data-ttu-id="91249-107">Os seguintes elementos de perfil de WLAN \_ não têm suporte no Windows XP com SP3 ou API de LAN sem fio para Windows XP com SP2:</span><span class="sxs-lookup"><span data-stu-id="91249-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="91249-108">conectividade (IHV)</span><span class="sxs-lookup"><span data-stu-id="91249-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="91249-109">IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="91249-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="91249-110">OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="91249-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="91249-111">phyType (conectividade)</span><span class="sxs-lookup"><span data-stu-id="91249-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="91249-112">PMKCacheMode (segurança)</span><span class="sxs-lookup"><span data-stu-id="91249-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="91249-113">PMKCacheSize (segurança)</span><span class="sxs-lookup"><span data-stu-id="91249-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="91249-114">PMKCacheTTL (segurança)</span><span class="sxs-lookup"><span data-stu-id="91249-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="91249-115">preAuthMode (segurança)</span><span class="sxs-lookup"><span data-stu-id="91249-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="91249-116">preAuthThrottle (segurança)</span><span class="sxs-lookup"><span data-stu-id="91249-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="91249-117">segurança (IHV)</span><span class="sxs-lookup"><span data-stu-id="91249-117">security (IHV)</span></span>
-   <span data-ttu-id="91249-118">tipo (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="91249-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="91249-119">useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="91249-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="91249-120">A tabela a seguir mostra os \_ elementos de perfil de WLAN com valores restritos para o Windows XP com SP3 e a API de LAN sem fio para Windows XP com SP2:</span><span class="sxs-lookup"><span data-stu-id="91249-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="91249-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="91249-121">Element</span></span>                                                                               | <span data-ttu-id="91249-122">Constraint</span><span class="sxs-lookup"><span data-stu-id="91249-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91249-123">**nome (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="91249-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="91249-124">O elemento Name é ignorado quando o perfil é salvo no repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="91249-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="91249-125">O nome do perfil é derivado automaticamente do SSID da rede.</span><span class="sxs-lookup"><span data-stu-id="91249-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="91249-126">Para perfis de rede de infraestrutura, o nome do perfil é o SSID da rede.</span><span class="sxs-lookup"><span data-stu-id="91249-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="91249-127">Para perfis de rede ad hoc, o nome do perfil é o SSID da rede ad hoc seguida por `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="91249-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="91249-128">**protegido (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="91249-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="91249-129">Deve ter um valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="91249-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="91249-130">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="91249-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="91249-131">Restrito a um elemento [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) filho.</span><span class="sxs-lookup"><span data-stu-id="91249-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="91249-132">Suporte a OneX</span><span class="sxs-lookup"><span data-stu-id="91249-132">OneX Support</span></span>

<span data-ttu-id="91249-133">Somente o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) tem suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="91249-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="91249-134">Outros elementos OneX, se presentes em um perfil, serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="91249-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91249-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91249-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91249-136">Sobre a API Wi-Fi nativa</span><span class="sxs-lookup"><span data-stu-id="91249-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="91249-137">Suporte nativo à API WiFi no Windows XP</span><span class="sxs-lookup"><span data-stu-id="91249-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



