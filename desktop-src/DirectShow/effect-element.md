---
description: O elemento Effect define um objeto de efeito de áudio ou vídeo. Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751231"
---
# <a name="effect-element"></a><span data-ttu-id="1b099-104">Elemento Effect</span><span class="sxs-lookup"><span data-stu-id="1b099-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="1b099-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1b099-105">\[Deprecated.</span></span> <span data-ttu-id="1b099-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b099-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1b099-107">O `effect` elemento define um objeto de efeito de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b099-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="1b099-108">Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).</span><span class="sxs-lookup"><span data-stu-id="1b099-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="1b099-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b099-109">Attributes</span></span>

<span data-ttu-id="1b099-110">[**CLSID**](clsid-attribute.md), [**Bloquear**](lock-attribute.md), [**ativar mudo**](mute-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nome de usuário**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="1b099-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="1b099-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="1b099-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b099-112">Pai</span><span class="sxs-lookup"><span data-stu-id="1b099-112">Parent</span></span>   | <span data-ttu-id="1b099-113">[**composto**](composite-element.md), [**Agrupar**](group-element.md), [**recortar**](clip-element.md), [**acompanhar**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="1b099-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="1b099-114">Children</span><span class="sxs-lookup"><span data-stu-id="1b099-114">Children</span></span> | [<span data-ttu-id="1b099-115">**param**</span><span class="sxs-lookup"><span data-stu-id="1b099-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="1b099-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b099-116">Remarks</span></span>

<span data-ttu-id="1b099-117">O atributo **CLSID** especifica o subobjeto que cria o efeito.</span><span class="sxs-lookup"><span data-stu-id="1b099-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="1b099-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b099-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="1b099-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b099-119">Requirements</span></span>



| <span data-ttu-id="1b099-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b099-120">Requirement</span></span> | <span data-ttu-id="1b099-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1b099-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b099-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b099-122">Header</span></span><br/> | <dl> <span data-ttu-id="1b099-123"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b099-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b099-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b099-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b099-125">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="1b099-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




