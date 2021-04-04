---
description: Especifica um provedor de rastreamento (ETW ou WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: elemento Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647749"
---
# <a name="provider-element"></a><span data-ttu-id="e1ae5-103">elemento Provider</span><span class="sxs-lookup"><span data-stu-id="e1ae5-103">provider element</span></span>

<span data-ttu-id="e1ae5-104">Especifica um provedor de rastreamento (ETW ou WPP) para [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="e1ae5-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="e1ae5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e1ae5-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="e1ae5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1ae5-106">Attributes</span></span>



| <span data-ttu-id="e1ae5-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="e1ae5-107">Attribute</span></span>            | <span data-ttu-id="e1ae5-108">Type</span><span class="sxs-lookup"><span data-stu-id="e1ae5-108">Type</span></span>             | <span data-ttu-id="e1ae5-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e1ae5-109">Required</span></span>       | <span data-ttu-id="e1ae5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae5-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="e1ae5-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="e1ae5-111">**ID**</span></span><br/>    | <span data-ttu-id="e1ae5-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="e1ae5-112">CDATA</span></span><br/> | <span data-ttu-id="e1ae5-113">Sim</span><span class="sxs-lookup"><span data-stu-id="e1ae5-113">Yes</span></span><br/> | <span data-ttu-id="e1ae5-114">O nome ou GUID do provedor.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="e1ae5-115">**level**</span><span class="sxs-lookup"><span data-stu-id="e1ae5-115">**level**</span></span><br/> | <span data-ttu-id="e1ae5-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="e1ae5-116">CDATA</span></span><br/> | <span data-ttu-id="e1ae5-117">Sim</span><span class="sxs-lookup"><span data-stu-id="e1ae5-117">Yes</span></span><br/> | <span data-ttu-id="e1ae5-118">O nível de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="e1ae5-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="e1ae5-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e1ae5-119">Child elements</span></span>



| <span data-ttu-id="e1ae5-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae5-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="e1ae5-121">**chaves**</span><span class="sxs-lookup"><span data-stu-id="e1ae5-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="e1ae5-122">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="e1ae5-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="e1ae5-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e1ae5-123">Parent elements</span></span>



| <span data-ttu-id="e1ae5-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae5-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="e1ae5-125">**fornecedor**</span><span class="sxs-lookup"><span data-stu-id="e1ae5-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="e1ae5-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e1ae5-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="e1ae5-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="e1ae5-127">Can be empty</span></span> | <span data-ttu-id="e1ae5-128">Não</span><span class="sxs-lookup"><span data-stu-id="e1ae5-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="e1ae5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1ae5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ae5-130">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="e1ae5-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




