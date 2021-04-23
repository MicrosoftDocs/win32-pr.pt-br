---
description: O elemento Effect define um objeto de efeito de áudio ou vídeo. Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908653"
---
# <a name="effect-element"></a><span data-ttu-id="f5c0c-104">Elemento Effect</span><span class="sxs-lookup"><span data-stu-id="f5c0c-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="f5c0c-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f5c0c-105">\[Deprecated.</span></span> <span data-ttu-id="f5c0c-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5c0c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5c0c-107">O `effect` elemento define um objeto de efeito de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5c0c-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="f5c0c-108">Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).</span><span class="sxs-lookup"><span data-stu-id="f5c0c-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="f5c0c-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5c0c-109">Attributes</span></span>

<span data-ttu-id="f5c0c-110">[**CLSID**](clsid-attribute.md), [**Bloquear**](lock-attribute.md), [**ativar mudo**](mute-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nome de usuário**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f5c0c-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="f5c0c-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="f5c0c-111">Parent/Child Information</span></span>



| <span data-ttu-id="f5c0c-112">Label</span><span class="sxs-lookup"><span data-stu-id="f5c0c-112">Label</span></span> | <span data-ttu-id="f5c0c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c0c-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c0c-114">Pai</span><span class="sxs-lookup"><span data-stu-id="f5c0c-114">Parent</span></span>   | <span data-ttu-id="f5c0c-115">[**composto**](composite-element.md), [**Agrupar**](group-element.md), [**recortar**](clip-element.md), [**acompanhar**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="f5c0c-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="f5c0c-116">Children</span><span class="sxs-lookup"><span data-stu-id="f5c0c-116">Children</span></span> | [<span data-ttu-id="f5c0c-117">**param**</span><span class="sxs-lookup"><span data-stu-id="f5c0c-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f5c0c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5c0c-118">Remarks</span></span>

<span data-ttu-id="f5c0c-119">O atributo **CLSID** especifica o subobjeto que cria o efeito.</span><span class="sxs-lookup"><span data-stu-id="f5c0c-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="f5c0c-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5c0c-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="f5c0c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c0c-121">Requirements</span></span>



| <span data-ttu-id="f5c0c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c0c-122">Requirement</span></span> | <span data-ttu-id="f5c0c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c0c-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c0c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5c0c-124">Header</span></span><br/> | <dl> <span data-ttu-id="f5c0c-125"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c0c-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c0c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5c0c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c0c-127">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="f5c0c-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




