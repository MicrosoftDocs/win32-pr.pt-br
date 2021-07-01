---
description: Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119331"
---
# <a name="mfdetours-element"></a><span data-ttu-id="8d88a-103">elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="8d88a-103">mfdetours element</span></span>

<span data-ttu-id="8d88a-104">Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="8d88a-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="8d88a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8d88a-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="8d88a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d88a-106">Attributes</span></span>



| <span data-ttu-id="8d88a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="8d88a-107">Attribute</span></span>            | <span data-ttu-id="8d88a-108">Type</span><span class="sxs-lookup"><span data-stu-id="8d88a-108">Type</span></span>             | <span data-ttu-id="8d88a-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8d88a-109">Required</span></span>       | <span data-ttu-id="8d88a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d88a-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="8d88a-111">**level**</span><span class="sxs-lookup"><span data-stu-id="8d88a-111">**level**</span></span><br/> | <span data-ttu-id="8d88a-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="8d88a-112">CDATA</span></span><br/> | <span data-ttu-id="8d88a-113">Sim</span><span class="sxs-lookup"><span data-stu-id="8d88a-113">Yes</span></span><br/> | <span data-ttu-id="8d88a-114">O nível de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="8d88a-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8d88a-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8d88a-115">Child elements</span></span>



| <span data-ttu-id="8d88a-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d88a-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="8d88a-117">**chaves**</span><span class="sxs-lookup"><span data-stu-id="8d88a-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="8d88a-118">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="8d88a-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="8d88a-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8d88a-119">Parent elements</span></span>

| <span data-ttu-id="8d88a-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d88a-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="8d88a-121">**fornecedor**</span><span class="sxs-lookup"><span data-stu-id="8d88a-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="8d88a-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8d88a-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="8d88a-123">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="8d88a-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="8d88a-124">Não</span><span class="sxs-lookup"><span data-stu-id="8d88a-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="8d88a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d88a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d88a-126">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="8d88a-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




