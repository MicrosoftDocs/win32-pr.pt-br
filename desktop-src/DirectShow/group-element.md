---
description: O elemento Group define um grupo, o objeto de nível superior em uma linha do tempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920049"
---
# <a name="group-element"></a><span data-ttu-id="f53d8-103">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="f53d8-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="f53d8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f53d8-104">\[Deprecated.</span></span> <span data-ttu-id="f53d8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f53d8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f53d8-106">O elemento **Group** define um grupo, o objeto de nível superior em uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="f53d8-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="f53d8-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f53d8-107">Attributes</span></span>

<span data-ttu-id="f53d8-108">[**bitdepth**](bitdepth-attribute.md), [**buffer**](buffering-attribute.md), [**taxa de quadros**](framerate-attribute.md), [**altura**](height-attribute.md), [**bloqueio**](lock-attribute.md), [**mudo**](mute-attribute.md), [**nome**](name-attribute.md), [**modo de exibição**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**tipo**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nome de usuário**](username-attribute.md), [**largura**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f53d8-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="f53d8-109">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="f53d8-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53d8-110">Pai</span><span class="sxs-lookup"><span data-stu-id="f53d8-110">Parent</span></span>   | [<span data-ttu-id="f53d8-111">**linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="f53d8-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="f53d8-112">Children</span><span class="sxs-lookup"><span data-stu-id="f53d8-112">Children</span></span> | <span data-ttu-id="f53d8-113">[**composto**](composite-element.md), [**efeito**](effect-element.md), [**faixa**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="f53d8-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f53d8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f53d8-114">Remarks</span></span>

<span data-ttu-id="f53d8-115">Dentro de um `group` elemento, a prioridade de camadas aninhadas é determinada implicitamente pela ordem em que aparecem dentro do elemento.</span><span class="sxs-lookup"><span data-stu-id="f53d8-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="f53d8-116">A primeira camada tem a prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.</span><span class="sxs-lookup"><span data-stu-id="f53d8-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="f53d8-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f53d8-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="f53d8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f53d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53d8-119">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="f53d8-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



