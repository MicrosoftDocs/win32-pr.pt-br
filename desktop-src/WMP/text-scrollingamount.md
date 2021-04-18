---
title: TEXT. scrollingAmount
description: O atributo scrollingAmount especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT. scrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759586"
---
# <a name="textscrollingamount"></a><span data-ttu-id="7ffcb-104">TEXT. scrollingAmount</span><span class="sxs-lookup"><span data-stu-id="7ffcb-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="7ffcb-105">O atributo **scrollingAmount** especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="7ffcb-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7ffcb-106">Possible Values</span></span>

<span data-ttu-id="7ffcb-107">Esse atributo é um **número** de leitura/gravação positivo (**int**) com um valor padrão de 6.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffcb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ffcb-108">Remarks</span></span>

<span data-ttu-id="7ffcb-109">Para uma rolagem suave, **scrollingAmount** deve ser pequeno.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="7ffcb-110">Para um desenho rápido com grandes intervalos, o **scrollingAmount** deve ser maior.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="7ffcb-111">Se **rolagem** = "false", **scrollingAmount** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="7ffcb-112">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="7ffcb-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffcb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ffcb-113">Requirements</span></span>



| <span data-ttu-id="7ffcb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ffcb-114">Requirement</span></span> | <span data-ttu-id="7ffcb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7ffcb-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7ffcb-116">Versão</span><span class="sxs-lookup"><span data-stu-id="7ffcb-116">Version</span></span><br/> | <span data-ttu-id="7ffcb-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7ffcb-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ffcb-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ffcb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffcb-119">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="7ffcb-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="7ffcb-120">**TEXTO. rolagem**</span><span class="sxs-lookup"><span data-stu-id="7ffcb-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





