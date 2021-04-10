---
description: Contém uma lista de provedores de rastreamento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164893"
---
# <a name="providers-element"></a><span data-ttu-id="a1f42-103">elemento providers</span><span class="sxs-lookup"><span data-stu-id="a1f42-103">providers element</span></span>

<span data-ttu-id="a1f42-104">Contém uma lista de provedores de rastreamento para [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="a1f42-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="a1f42-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a1f42-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="a1f42-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1f42-106">Attributes</span></span>

<span data-ttu-id="a1f42-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="a1f42-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a1f42-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a1f42-108">Child elements</span></span>



| <span data-ttu-id="a1f42-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a1f42-109">Element</span></span>                                   | <span data-ttu-id="a1f42-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1f42-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1f42-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="a1f42-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="a1f42-112">Especifica o provedor de destours Media Foundation, que rastreia Media Foundation chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="a1f42-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="a1f42-113">**operador**</span><span class="sxs-lookup"><span data-stu-id="a1f42-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="a1f42-114">Especifica um provedor de rastreamento (ETW ou WPP).</span><span class="sxs-lookup"><span data-stu-id="a1f42-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="a1f42-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="a1f42-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="a1f42-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a1f42-116">Parent elements</span></span>

<span data-ttu-id="a1f42-117">Não há elementos pai.</span><span class="sxs-lookup"><span data-stu-id="a1f42-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="a1f42-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a1f42-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="a1f42-119">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a1f42-119">Can be empty</span></span> | <span data-ttu-id="a1f42-120">Yes</span><span class="sxs-lookup"><span data-stu-id="a1f42-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="a1f42-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1f42-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f42-122">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="a1f42-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




