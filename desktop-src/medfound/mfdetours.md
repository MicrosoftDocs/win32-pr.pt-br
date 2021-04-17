---
description: Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762154"
---
# <a name="mfdetours-element"></a><span data-ttu-id="b0fa7-103">elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="b0fa7-103">mfdetours element</span></span>

<span data-ttu-id="b0fa7-104">Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="b0fa7-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="b0fa7-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b0fa7-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="b0fa7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0fa7-106">Attributes</span></span>



| <span data-ttu-id="b0fa7-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b0fa7-107">Attribute</span></span>            | <span data-ttu-id="b0fa7-108">Type</span><span class="sxs-lookup"><span data-stu-id="b0fa7-108">Type</span></span>             | <span data-ttu-id="b0fa7-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0fa7-109">Required</span></span>       | <span data-ttu-id="b0fa7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0fa7-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="b0fa7-111">**level**</span><span class="sxs-lookup"><span data-stu-id="b0fa7-111">**level**</span></span><br/> | <span data-ttu-id="b0fa7-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="b0fa7-112">CDATA</span></span><br/> | <span data-ttu-id="b0fa7-113">Sim</span><span class="sxs-lookup"><span data-stu-id="b0fa7-113">Yes</span></span><br/> | <span data-ttu-id="b0fa7-114">O nível de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b0fa7-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b0fa7-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b0fa7-115">Child elements</span></span>



| <span data-ttu-id="b0fa7-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0fa7-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="b0fa7-117">**chaves**</span><span class="sxs-lookup"><span data-stu-id="b0fa7-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b0fa7-118">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="b0fa7-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="b0fa7-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b0fa7-119">Parent elements</span></span>



| <span data-ttu-id="b0fa7-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0fa7-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="b0fa7-121">**fornecedor**</span><span class="sxs-lookup"><span data-stu-id="b0fa7-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="b0fa7-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b0fa7-122">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="b0fa7-123">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="b0fa7-123">Can be empty</span></span> | <span data-ttu-id="b0fa7-124">Não</span><span class="sxs-lookup"><span data-stu-id="b0fa7-124">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="b0fa7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0fa7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fa7-126">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="b0fa7-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




