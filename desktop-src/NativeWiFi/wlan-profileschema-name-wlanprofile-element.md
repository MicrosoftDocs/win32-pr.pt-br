---
description: Contém o nome de um perfil de LAN sem fio.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Elemento Name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502234"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="fc3bc-103">Elemento Name (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="fc3bc-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="fc3bc-104">O elemento Name (WLANProfile) contém o nome de um perfil de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="fc3bc-105">O elemento **Name** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3bc-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc3bc-106">Remarks</span></span>

<span data-ttu-id="fc3bc-107">Os nomes diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-107">Names are case-sensitive.</span></span>

<span data-ttu-id="fc3bc-108">Para o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2), o elemento Name é ignorado quando o perfil é salvo no repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="fc3bc-109">O nome do perfil é derivado do SSID da rede.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="fc3bc-110">Para perfis de rede de infraestrutura, o nome do perfil é o SSID da rede.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="fc3bc-111">Para perfis de rede ad hoc, o nome do perfil é o SSID da rede ad hoc seguida por `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="fc3bc-112">Os caracteres de escape XML, como &, não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="fc3bc-113">Evite usar caracteres de escape XML em nomes SSID para perfis implantados no Windows XP com SP3 ou API de LAN sem fio para Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="fc3bc-114">Para qualquer perfil de rede destinado a uso somente no Windows Vista ou no Windows Server 2008, o nome pode ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="fc3bc-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc3bc-115">Examples</span></span>

<span data-ttu-id="fc3bc-116">Para exibir perfis de exemplo que usam o elemento **Name** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fc3bc-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc3bc-117">Requirements</span></span>



| <span data-ttu-id="fc3bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3bc-118">Requirement</span></span> | <span data-ttu-id="fc3bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fc3bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fc3bc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc3bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3bc-121">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="fc3bc-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fc3bc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc3bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3bc-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc3bc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fc3bc-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fc3bc-124">Redistributable</span></span><br/>          | <span data-ttu-id="fc3bc-125">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="fc3bc-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fc3bc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc3bc-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc3bc-127">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="fc3bc-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fc3bc-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fc3bc-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fc3bc-129">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="fc3bc-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fc3bc-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fc3bc-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




