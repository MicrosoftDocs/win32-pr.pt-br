---
description: Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Elemento useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921955"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="92e76-103">Elemento useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="92e76-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="92e76-104">O elemento **useMSOneX** (IHV) especifica a origem das configurações de segurança 802.1 x usadas por um componente de segurança do IHV.</span><span class="sxs-lookup"><span data-stu-id="92e76-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="92e76-105">Quando **useMSOneX** é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92e76-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="92e76-106">Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="92e76-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="92e76-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="92e76-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="92e76-108">O elemento é definido pelo elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="92e76-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e76-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e76-109">Requirements</span></span>



| <span data-ttu-id="92e76-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e76-110">Requirement</span></span> | <span data-ttu-id="92e76-111">Valor</span><span class="sxs-lookup"><span data-stu-id="92e76-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92e76-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e76-112">Minimum supported client</span></span><br/> | <span data-ttu-id="92e76-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92e76-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92e76-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e76-114">Minimum supported server</span></span><br/> | <span data-ttu-id="92e76-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92e76-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92e76-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="92e76-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="92e76-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="92e76-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="92e76-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="92e76-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="92e76-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="92e76-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="92e76-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="92e76-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




