---
title: TEXT. scrollingDelay
description: O atributo scrollingDelay especifica ou recupera o intervalo de tempo entre movimentos de rolagem.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- TEXT. scrollingDelay Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758718"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="6856a-104">TEXT. scrollingDelay</span><span class="sxs-lookup"><span data-stu-id="6856a-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="6856a-105">O atributo **scrollingDelay** especifica ou recupera o intervalo de tempo entre movimentos de rolagem.</span><span class="sxs-lookup"><span data-stu-id="6856a-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="6856a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6856a-106">Possible Values</span></span>

<span data-ttu-id="6856a-107">Esse atributo é um **número** de leitura/gravação (**int**) que especifica o atraso em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="6856a-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="6856a-108">Ele tem um valor mínimo de 30 e um valor padrão de 85.</span><span class="sxs-lookup"><span data-stu-id="6856a-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="6856a-109">Se um valor menor que o mínimo for especificado, o padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="6856a-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6856a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6856a-110">Remarks</span></span>

<span data-ttu-id="6856a-111">Se a **rolagem** for definida como false, **scrollingDelay** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="6856a-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="6856a-112">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="6856a-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6856a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6856a-113">Requirements</span></span>



| <span data-ttu-id="6856a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6856a-114">Requirement</span></span> | <span data-ttu-id="6856a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6856a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6856a-116">Versão</span><span class="sxs-lookup"><span data-stu-id="6856a-116">Version</span></span><br/> | <span data-ttu-id="6856a-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6856a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6856a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6856a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6856a-119">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="6856a-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="6856a-120">**TEXTO. rolagem**</span><span class="sxs-lookup"><span data-stu-id="6856a-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





