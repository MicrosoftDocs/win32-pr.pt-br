---
title: DownloadItem. downloadstate
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade downloadstate recupera o estado do download.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadstate Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794487"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="91f60-106">DownloadItem. downloadstate</span><span class="sxs-lookup"><span data-stu-id="91f60-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="91f60-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="91f60-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="91f60-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="91f60-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="91f60-109">A propriedade **downloadstate** recupera o estado do download.</span><span class="sxs-lookup"><span data-stu-id="91f60-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f60-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f60-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="91f60-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="91f60-111">Possible Values</span></span>

<span data-ttu-id="91f60-112">Essa propriedade é um **número** somente leitura que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="91f60-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="91f60-113">Valor</span><span class="sxs-lookup"><span data-stu-id="91f60-113">Value</span></span> | <span data-ttu-id="91f60-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="91f60-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="91f60-115">0</span><span class="sxs-lookup"><span data-stu-id="91f60-115">0</span></span>     | <span data-ttu-id="91f60-116">Baixando</span><span class="sxs-lookup"><span data-stu-id="91f60-116">Downloading</span></span> |
| <span data-ttu-id="91f60-117">1</span><span class="sxs-lookup"><span data-stu-id="91f60-117">1</span></span>     | <span data-ttu-id="91f60-118">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="91f60-118">Paused</span></span>      |
| <span data-ttu-id="91f60-119">2</span><span class="sxs-lookup"><span data-stu-id="91f60-119">2</span></span>     | <span data-ttu-id="91f60-120">Processing</span><span class="sxs-lookup"><span data-stu-id="91f60-120">Processing</span></span>  |
| <span data-ttu-id="91f60-121">3</span><span class="sxs-lookup"><span data-stu-id="91f60-121">3</span></span>     | <span data-ttu-id="91f60-122">Concluído</span><span class="sxs-lookup"><span data-stu-id="91f60-122">Completed</span></span>   |
| <span data-ttu-id="91f60-123">4</span><span class="sxs-lookup"><span data-stu-id="91f60-123">4</span></span>     | <span data-ttu-id="91f60-124">Canceled</span><span class="sxs-lookup"><span data-stu-id="91f60-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="91f60-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="91f60-125">Remarks</span></span>

<span data-ttu-id="91f60-126">Os Estados de download podem ocorrer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="91f60-126">Download states can occur in any order.</span></span> <span data-ttu-id="91f60-127">Não grave o código que depende da ocorrência de qualquer estado de download específico.</span><span class="sxs-lookup"><span data-stu-id="91f60-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f60-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91f60-128">Requirements</span></span>



| <span data-ttu-id="91f60-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="91f60-129">Requirement</span></span> | <span data-ttu-id="91f60-130">Valor</span><span class="sxs-lookup"><span data-stu-id="91f60-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91f60-131">Versão</span><span class="sxs-lookup"><span data-stu-id="91f60-131">Version</span></span><br/> | <span data-ttu-id="91f60-132">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="91f60-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="91f60-133">DLL</span><span class="sxs-lookup"><span data-stu-id="91f60-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="91f60-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91f60-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f60-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="91f60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f60-136">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="91f60-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





