---
title: Elemento HTMLView
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento HTMLView especifica a URL base de uma página da Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView do Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800129"
---
# <a name="htmlview-element"></a><span data-ttu-id="5bc85-106">Elemento HTMLView</span><span class="sxs-lookup"><span data-stu-id="5bc85-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="5bc85-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5bc85-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5bc85-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5bc85-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5bc85-109">O elemento **HtmlView** especifica a URL base de uma página da Web HtmlView.</span><span class="sxs-lookup"><span data-stu-id="5bc85-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="5bc85-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bc85-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="5bc85-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="5bc85-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="5bc85-112">URL base para a página da Web do HTMLView que o Windows Media Player exibe.</span><span class="sxs-lookup"><span data-stu-id="5bc85-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="5bc85-113">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="5bc85-113">Parent/Child Elements</span></span>



| <span data-ttu-id="5bc85-114">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="5bc85-114">Hierarchy</span></span>       | <span data-ttu-id="5bc85-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5bc85-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="5bc85-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5bc85-116">Parent elements</span></span> | <span data-ttu-id="5bc85-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5bc85-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="5bc85-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5bc85-118">Child elements</span></span>  | <span data-ttu-id="5bc85-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5bc85-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="5bc85-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bc85-120">Remarks</span></span>

<span data-ttu-id="5bc85-121">Você pode usar esse elemento para integrar o recurso HTMLView com sua loja online.</span><span class="sxs-lookup"><span data-stu-id="5bc85-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="5bc85-122">Se o domínio da URL especificado pelo repositório online atual corresponder ao da página da Web do HTMLView, a opção de **executar agora** acontece sem intervenção do usuário e o conteúdo de HtmlView é exibido.</span><span class="sxs-lookup"><span data-stu-id="5bc85-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="5bc85-123">Caso contrário, o Windows Media Player solicita ao usuário permissão para mostrar o conteúdo do HTMLView.</span><span class="sxs-lookup"><span data-stu-id="5bc85-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="5bc85-124">Por exemplo, se a URL para a página da Web HTMLView for https://www.proseware.com/html/HTMLView.htm e a URL para o atributo **BaseURL** for especificada como https://www.proseware.com , a página da Web HtmlView será exibida sem avisar o usuário.</span><span class="sxs-lookup"><span data-stu-id="5bc85-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc85-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc85-125">Requirements</span></span>



| <span data-ttu-id="5bc85-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc85-126">Requirement</span></span> | <span data-ttu-id="5bc85-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5bc85-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="5bc85-128">Versão</span><span class="sxs-lookup"><span data-stu-id="5bc85-128">Version</span></span><br/> | <span data-ttu-id="5bc85-129">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5bc85-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bc85-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc85-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc85-131">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="5bc85-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="5bc85-132">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5bc85-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5bc85-133">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5bc85-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5bc85-134">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="5bc85-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="5bc85-135">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="5bc85-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





