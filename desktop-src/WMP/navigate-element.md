---
title: Elemento Navigate
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento Navigate especifica uma URL usada por chamadas para external. NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Navegar no elemento Windows Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747688"
---
# <a name="navigate-element"></a><span data-ttu-id="7bf01-106">Elemento Navigate</span><span class="sxs-lookup"><span data-stu-id="7bf01-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="7bf01-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="7bf01-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7bf01-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="7bf01-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7bf01-109">O elemento **Navigate** especifica uma URL usada por chamadas para **external. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="7bf01-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="7bf01-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7bf01-110">Attributes</span></span>



| <span data-ttu-id="7bf01-111">Termo</span><span class="sxs-lookup"><span data-stu-id="7bf01-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="7bf01-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bf01-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf01-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="7bf01-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="7bf01-114">URL totalmente qualificada para a página da Web na qual navegar.</span><span class="sxs-lookup"><span data-stu-id="7bf01-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="7bf01-115">**NavigateTaskPaneURL** pode acrescentar uma cadeia de caracteres de consulta a essa URL.</span><span class="sxs-lookup"><span data-stu-id="7bf01-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="7bf01-116">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="7bf01-116">Parent/Child Elements</span></span>



| <span data-ttu-id="7bf01-117">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="7bf01-117">Hierarchy</span></span>       | <span data-ttu-id="7bf01-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="7bf01-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="7bf01-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7bf01-119">Parent elements</span></span> | <span data-ttu-id="7bf01-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="7bf01-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="7bf01-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7bf01-121">Child elements</span></span>  | <span data-ttu-id="7bf01-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7bf01-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="7bf01-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bf01-123">Requirements</span></span>



| <span data-ttu-id="7bf01-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf01-124">Requirement</span></span> | <span data-ttu-id="7bf01-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7bf01-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="7bf01-126">Versão</span><span class="sxs-lookup"><span data-stu-id="7bf01-126">Version</span></span><br/> | <span data-ttu-id="7bf01-127">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7bf01-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7bf01-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bf01-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf01-129">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="7bf01-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="7bf01-130">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7bf01-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="7bf01-131">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="7bf01-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="7bf01-132">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="7bf01-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





