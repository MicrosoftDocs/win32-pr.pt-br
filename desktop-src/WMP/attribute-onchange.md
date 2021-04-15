---
title: attribute_onchange
description: Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e \ 0034; OnChange \ 0034;, como \ 0034; valor \_ onChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange o Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761489"
---
# <a name="attribute_onchange"></a><span data-ttu-id="9213e-105">atributo \_ onChange</span><span class="sxs-lookup"><span data-stu-id="9213e-105">attribute\_onchange</span></span>

<span data-ttu-id="9213e-106">Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="9213e-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="9213e-107">O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e "OnChange", como "valor \_ onChange".</span><span class="sxs-lookup"><span data-stu-id="9213e-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="9213e-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9213e-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="9213e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9213e-109">Requirements</span></span>



| <span data-ttu-id="9213e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9213e-110">Requirement</span></span> | <span data-ttu-id="9213e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9213e-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="9213e-112">Versão</span><span class="sxs-lookup"><span data-stu-id="9213e-112">Version</span></span><br/> | <span data-ttu-id="9213e-113">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9213e-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9213e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="9213e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9213e-115">**Manipuladores de eventos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="9213e-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





