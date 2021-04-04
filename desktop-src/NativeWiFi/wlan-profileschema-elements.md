---
description: O \_ esquema de perfil WLAN define os elementos a seguir.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Elementos do esquema de WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647351"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="e3879-103">\_Elementos do esquema do perfil WLAN</span><span class="sxs-lookup"><span data-stu-id="e3879-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="e3879-104">O \_ esquema de perfil WLAN define os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3879-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="e3879-105">A maioria dos elementos está no namespace `https://www.microsoft.com/networking/WLAN/profile/v1` , com exceção de [**fipsmode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), que está no namespace `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="e3879-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="e3879-106">A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3879-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="e3879-107">A ordem dos elementos é imposta.</span><span class="sxs-lookup"><span data-stu-id="e3879-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="e3879-108">Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="e3879-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="e3879-109">Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil sem fio, pois os elementos podem ser adicionados em **xs: qualquer** ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="e3879-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="e3879-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="e3879-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="e3879-111">**nome (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="e3879-112">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="e3879-113">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="e3879-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="e3879-114">**Hex (SSID)**</span><span class="sxs-lookup"><span data-stu-id="e3879-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="e3879-115">**nome (SSID)**</span><span class="sxs-lookup"><span data-stu-id="e3879-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="e3879-116">**não difusão (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="e3879-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="e3879-117">**Hotspot2 (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="e3879-118">**Nome_do_domínio (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="e3879-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="e3879-119">**NAIRealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="e3879-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="e3879-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="e3879-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="e3879-121">**RoamingConsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="e3879-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="e3879-122">**ConnectionType (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="e3879-123">**ConnectionMode (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="e3879-124">**AutoSwitch (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="e3879-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="e3879-126">**conectividade (MSM)**</span><span class="sxs-lookup"><span data-stu-id="e3879-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="e3879-127">**phyType (conectividade)**</span><span class="sxs-lookup"><span data-stu-id="e3879-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="e3879-128">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="e3879-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="e3879-129">**authEncryption (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="e3879-130">**autenticação (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="e3879-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="e3879-131">**criptografia (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="e3879-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="e3879-132">**useOneX (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="e3879-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="e3879-133">**FIPSmode (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="e3879-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="e3879-134">**sharedKey (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="e3879-135">**KeyType (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="e3879-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="e3879-136">**protegido (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="e3879-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="e3879-137">**keymaterial (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="e3879-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="e3879-138">**KeyIndex (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="e3879-139">**PMKCacheMode (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="e3879-140">**PMKCacheTTL (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="e3879-141">**PMKCacheSize (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="e3879-142">**preAuthMode (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="e3879-143">**preAuthThrottle (segurança)**</span><span class="sxs-lookup"><span data-stu-id="e3879-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="e3879-144">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e3879-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="e3879-145">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="e3879-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="e3879-146">**OUI (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="e3879-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="e3879-147">**tipo (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="e3879-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="e3879-148">**conectividade (IHV)**</span><span class="sxs-lookup"><span data-stu-id="e3879-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="e3879-149">**segurança (IHV)**</span><span class="sxs-lookup"><span data-stu-id="e3879-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="e3879-150">**useMSOneX (IHV)**</span><span class="sxs-lookup"><span data-stu-id="e3879-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



