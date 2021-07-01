---
description: Contém uma lista de provedores de rastreamento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118481"
---
# <a name="providers-element"></a><span data-ttu-id="e07f1-103">elemento providers</span><span class="sxs-lookup"><span data-stu-id="e07f1-103">providers element</span></span>

<span data-ttu-id="e07f1-104">Contém uma lista de provedores de rastreamento para [o MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="e07f1-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="e07f1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e07f1-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="e07f1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e07f1-106">Attributes</span></span>

<span data-ttu-id="e07f1-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="e07f1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e07f1-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e07f1-108">Child elements</span></span>



| <span data-ttu-id="e07f1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e07f1-109">Element</span></span>                                   | <span data-ttu-id="e07f1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e07f1-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e07f1-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="e07f1-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="e07f1-112">Especifica o provedor Media Foundation Detours, que Media Foundation chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="e07f1-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="e07f1-113">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="e07f1-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="e07f1-114">Especifica um provedor de rastreamento (ETW ou WPP).</span><span class="sxs-lookup"><span data-stu-id="e07f1-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="e07f1-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="e07f1-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="e07f1-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e07f1-116">Parent elements</span></span>

<span data-ttu-id="e07f1-117">Não há elementos pai.</span><span class="sxs-lookup"><span data-stu-id="e07f1-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="e07f1-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e07f1-118">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="e07f1-119">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="e07f1-119">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="e07f1-120">Sim</span><span class="sxs-lookup"><span data-stu-id="e07f1-120">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="e07f1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e07f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07f1-122">Arquivo de configuração do MFTrace</span><span class="sxs-lookup"><span data-stu-id="e07f1-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




