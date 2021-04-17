---
title: DownloadItem.sourceURL
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade sourceURL recupera a URL de origem do download.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- DownloadItem. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813171"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="6ae94-106">DownloadItem.sourceURL</span><span class="sxs-lookup"><span data-stu-id="6ae94-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="6ae94-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="6ae94-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6ae94-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="6ae94-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6ae94-109">A propriedade **sourceURL** recupera a URL de origem do download.</span><span class="sxs-lookup"><span data-stu-id="6ae94-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae94-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ae94-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="6ae94-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6ae94-111">Possible Values</span></span>

<span data-ttu-id="6ae94-112">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ae94-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae94-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ae94-113">Remarks</span></span>

<span data-ttu-id="6ae94-114">Somente os seguintes formatos de mídia digital podem ser baixados:</span><span class="sxs-lookup"><span data-stu-id="6ae94-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="6ae94-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="6ae94-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="6ae94-116">MP3</span><span class="sxs-lookup"><span data-stu-id="6ae94-116">MP3</span></span>
-   <span data-ttu-id="6ae94-117">Áudio do Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="6ae94-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="6ae94-118">Vídeo do Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="6ae94-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae94-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae94-119">Requirements</span></span>



| <span data-ttu-id="6ae94-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae94-120">Requirement</span></span> | <span data-ttu-id="6ae94-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6ae94-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae94-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6ae94-122">Version</span></span><br/> | <span data-ttu-id="6ae94-123">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6ae94-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6ae94-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae94-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ae94-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ae94-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae94-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ae94-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae94-127">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="6ae94-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





