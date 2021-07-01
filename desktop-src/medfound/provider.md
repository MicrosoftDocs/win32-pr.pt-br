---
description: Especifica um provedor de rastreamento (ETW ou WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: elemento provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118441"
---
# <a name="provider-element"></a><span data-ttu-id="ba6db-103">elemento provider</span><span class="sxs-lookup"><span data-stu-id="ba6db-103">provider element</span></span>

<span data-ttu-id="ba6db-104">Especifica um provedor de rastreamento (ETW ou WPP) para [MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="ba6db-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ba6db-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ba6db-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="ba6db-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba6db-106">Attributes</span></span>



| <span data-ttu-id="ba6db-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="ba6db-107">Attribute</span></span>            | <span data-ttu-id="ba6db-108">Type</span><span class="sxs-lookup"><span data-stu-id="ba6db-108">Type</span></span>             | <span data-ttu-id="ba6db-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ba6db-109">Required</span></span>       | <span data-ttu-id="ba6db-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba6db-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="ba6db-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="ba6db-111">**ID**</span></span><br/>    | <span data-ttu-id="ba6db-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="ba6db-112">CDATA</span></span><br/> | <span data-ttu-id="ba6db-113">Sim</span><span class="sxs-lookup"><span data-stu-id="ba6db-113">Yes</span></span><br/> | <span data-ttu-id="ba6db-114">O nome ou GUID do provedor.</span><span class="sxs-lookup"><span data-stu-id="ba6db-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="ba6db-115">**level**</span><span class="sxs-lookup"><span data-stu-id="ba6db-115">**level**</span></span><br/> | <span data-ttu-id="ba6db-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="ba6db-116">CDATA</span></span><br/> | <span data-ttu-id="ba6db-117">Sim</span><span class="sxs-lookup"><span data-stu-id="ba6db-117">Yes</span></span><br/> | <span data-ttu-id="ba6db-118">O nível de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ba6db-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="ba6db-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ba6db-119">Child elements</span></span>



| <span data-ttu-id="ba6db-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba6db-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="ba6db-121">**Palavra**</span><span class="sxs-lookup"><span data-stu-id="ba6db-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="ba6db-122">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="ba6db-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="ba6db-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ba6db-123">Parent elements</span></span>



| <span data-ttu-id="ba6db-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba6db-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="ba6db-125">**Provedores**</span><span class="sxs-lookup"><span data-stu-id="ba6db-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="ba6db-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ba6db-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="ba6db-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="ba6db-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="ba6db-128">Não</span><span class="sxs-lookup"><span data-stu-id="ba6db-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="ba6db-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba6db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6db-130">Arquivo de configuração do MFTrace</span><span class="sxs-lookup"><span data-stu-id="ba6db-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




