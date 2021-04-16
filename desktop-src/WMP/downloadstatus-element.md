---
title: Elemento DownloadStatus (msfeeds. h)
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Elemento DownloadStatus do Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758222"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="5858f-105">Elemento DownloadStatus</span><span class="sxs-lookup"><span data-stu-id="5858f-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="5858f-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5858f-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5858f-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5858f-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5858f-108">O elemento **DownloadStatus** especifica uma URL que o Windows Media Player exibe como um link para permitir que os usuários exibam o status de download.</span><span class="sxs-lookup"><span data-stu-id="5858f-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="5858f-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="5858f-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="5858f-110"><span id="URL"></span><span id="url"></span>URL</span><span class="sxs-lookup"><span data-stu-id="5858f-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="5858f-111">URL para a página da Web que a loja online exibe para mostrar o status de download para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5858f-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="5858f-112">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="5858f-112">Parent/Child Elements</span></span>



| <span data-ttu-id="5858f-113">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="5858f-113">Hierarchy</span></span>       | <span data-ttu-id="5858f-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="5858f-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="5858f-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5858f-115">Parent elements</span></span> | <span data-ttu-id="5858f-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5858f-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="5858f-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5858f-117">Child elements</span></span>  | <span data-ttu-id="5858f-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5858f-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="5858f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5858f-119">Remarks</span></span>

<span data-ttu-id="5858f-120">O Windows Media Player exibe uma mensagem para os usuários quando um download está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5858f-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="5858f-121">Se os serviços ativos atuais definirem uma URL de status de download, o usuário poderá clicar no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5858f-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="5858f-122">Quando o usuário clica na mensagem, o Player navega até a URL especificada pelo elemento **DownloadStatus** para que o repositório ativo atual possa fornecer detalhes sobre os downloads em andamento.</span><span class="sxs-lookup"><span data-stu-id="5858f-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="5858f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5858f-123">Requirements</span></span>



| <span data-ttu-id="5858f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5858f-124">Requirement</span></span> | <span data-ttu-id="5858f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5858f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5858f-126">Versão</span><span class="sxs-lookup"><span data-stu-id="5858f-126">Version</span></span><br/> | <span data-ttu-id="5858f-127">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5858f-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="5858f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5858f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5858f-129"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="5858f-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5858f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5858f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5858f-131">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5858f-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5858f-132">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5858f-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5858f-133">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="5858f-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





