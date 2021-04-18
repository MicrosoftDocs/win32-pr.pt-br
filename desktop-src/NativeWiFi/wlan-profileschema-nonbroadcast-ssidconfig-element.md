---
description: Indica se é para se conectar a uma rede oculta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonBroadcast (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766368"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="806cc-103">Elemento nonBroadcast (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="806cc-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="806cc-104">O elemento nonBroadcast (SSIDConfig) indica se uma rede oculta deve ser conectada.</span><span class="sxs-lookup"><span data-stu-id="806cc-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="806cc-105">Se uma rede não difundir seu SSID, ela é conhecida como rede oculta.</span><span class="sxs-lookup"><span data-stu-id="806cc-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="806cc-106">Se vários SSIDs forem definidos dentro do perfil, eles deverão ter o mesmo valor de não-difusão.</span><span class="sxs-lookup"><span data-stu-id="806cc-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="806cc-107">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como **ESS**, esse valor poderá ser "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="806cc-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="806cc-108">Se esse elemento não estiver presente, o valor padrão será "false".</span><span class="sxs-lookup"><span data-stu-id="806cc-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="806cc-109">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como **IBSS**, esse valor deverá ser "false".</span><span class="sxs-lookup"><span data-stu-id="806cc-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="806cc-110">Se esse elemento não estiver presente, o valor padrão será "false".</span><span class="sxs-lookup"><span data-stu-id="806cc-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="806cc-111">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="806cc-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="806cc-112">O elemento é definido pelo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="806cc-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="806cc-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="806cc-113">Examples</span></span>

<span data-ttu-id="806cc-114">Para exibir um perfil de exemplo que usa o elemento **nonBroadcast** , consulte [exemplo de perfil sem difusão](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="806cc-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="806cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806cc-115">Requirements</span></span>



| <span data-ttu-id="806cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="806cc-116">Requirement</span></span> | <span data-ttu-id="806cc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="806cc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="806cc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="806cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="806cc-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="806cc-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="806cc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="806cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="806cc-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="806cc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="806cc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="806cc-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="806cc-123">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="806cc-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="806cc-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="806cc-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="806cc-125">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="806cc-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="806cc-126">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="806cc-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




