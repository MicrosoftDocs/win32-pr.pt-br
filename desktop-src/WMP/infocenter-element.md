---
title: Elemento do InfoCenter
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento do InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento do centro de mídia do Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788158"
---
# <a name="infocenter-element"></a><span data-ttu-id="a6143-105">Elemento do InfoCenter</span><span class="sxs-lookup"><span data-stu-id="a6143-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="a6143-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="a6143-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a6143-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="a6143-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a6143-108">O elemento **InfoCenter** especifica a URL da página da Web que o Windows Media Player exibe no recurso de exibição do info Center de **agora em execução** quando o repositório online está ativo.</span><span class="sxs-lookup"><span data-stu-id="a6143-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="a6143-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6143-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a6143-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="a6143-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="a6143-111">URL da página da Web exibida pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a6143-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a6143-112">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="a6143-112">Parent/Child Elements</span></span>



| <span data-ttu-id="a6143-113">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="a6143-113">Hierarchy</span></span>       | <span data-ttu-id="a6143-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="a6143-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="a6143-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a6143-115">Parent elements</span></span> | <span data-ttu-id="a6143-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a6143-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="a6143-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a6143-117">Child elements</span></span>  | <span data-ttu-id="a6143-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a6143-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="a6143-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6143-119">Remarks</span></span>

<span data-ttu-id="a6143-120">O usuário controla quando a exibição do centro de informações está ativa.</span><span class="sxs-lookup"><span data-stu-id="a6143-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="a6143-121">Para recuperar informações sobre o item de mídia em execução no momento, você deve inserir uma instância do controle do Windows Media Player em sua página da Web e usar o modelo de objeto do Player.</span><span class="sxs-lookup"><span data-stu-id="a6143-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="a6143-122">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="a6143-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="a6143-123">Outros podem estar presentes para fins de compatibilidade herdada.</span><span class="sxs-lookup"><span data-stu-id="a6143-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="a6143-124">Nome</span><span class="sxs-lookup"><span data-stu-id="a6143-124">Name</span></span>         | <span data-ttu-id="a6143-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a6143-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6143-126">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="a6143-126">*geoid*</span></span>      | <span data-ttu-id="a6143-127">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6143-127">Windows geographical location ID.</span></span> <span data-ttu-id="a6143-128">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="a6143-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="a6143-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="a6143-129">*locale*</span></span>     | <span data-ttu-id="a6143-130">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a6143-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="a6143-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="a6143-131">*userlocale*</span></span> | <span data-ttu-id="a6143-132">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6143-132">Windows locale ID.</span></span> <span data-ttu-id="a6143-133">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="a6143-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="a6143-134">*version*</span><span class="sxs-lookup"><span data-stu-id="a6143-134">*version*</span></span>    | <span data-ttu-id="a6143-135">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="a6143-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a6143-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6143-136">Requirements</span></span>



| <span data-ttu-id="a6143-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6143-137">Requirement</span></span> | <span data-ttu-id="a6143-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a6143-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="a6143-139">Versão</span><span class="sxs-lookup"><span data-stu-id="a6143-139">Version</span></span><br/> | <span data-ttu-id="a6143-140">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a6143-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6143-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6143-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6143-142">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a6143-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="a6143-143">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="a6143-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a6143-144">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="a6143-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





