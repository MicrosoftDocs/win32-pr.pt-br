---
title: DownloadItem. Size
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade Size recupera o tamanho do download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. dimensionar o Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784902"
---
# <a name="downloaditemsize"></a><span data-ttu-id="9d930-106">DownloadItem. Size</span><span class="sxs-lookup"><span data-stu-id="9d930-106">DownloadItem.size</span></span>

> [!Note]  
> <span data-ttu-id="9d930-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="9d930-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9d930-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="9d930-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9d930-109">A propriedade **size** recupera o tamanho do download.</span><span class="sxs-lookup"><span data-stu-id="9d930-109">The **size** property retrieves the size of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d930-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d930-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a><span data-ttu-id="9d930-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9d930-111">Possible Values</span></span>

<span data-ttu-id="9d930-112">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="9d930-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d930-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d930-113">Requirements</span></span>



| <span data-ttu-id="9d930-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d930-114">Requirement</span></span> | <span data-ttu-id="9d930-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9d930-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d930-116">Versão</span><span class="sxs-lookup"><span data-stu-id="9d930-116">Version</span></span><br/> | <span data-ttu-id="9d930-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d930-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="9d930-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9d930-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d930-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d930-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d930-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d930-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d930-121">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="9d930-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="9d930-122">**DownloadItem. Progress**</span><span class="sxs-lookup"><span data-stu-id="9d930-122">**DownloadItem.progress**</span></span>](downloaditem-progress.md)
</dt> </dl>

 

 





