---
title: DownloadItem. Progress
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade Progress recupera o progresso do download em bytes.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem. Progress Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770506"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="de93d-106">DownloadItem. Progress</span><span class="sxs-lookup"><span data-stu-id="de93d-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="de93d-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="de93d-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="de93d-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="de93d-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="de93d-109">A propriedade **Progress** recupera o progresso do download em bytes.</span><span class="sxs-lookup"><span data-stu-id="de93d-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="de93d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="de93d-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="de93d-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="de93d-111">Possible Values</span></span>

<span data-ttu-id="de93d-112">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="de93d-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="de93d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de93d-113">Requirements</span></span>



| <span data-ttu-id="de93d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de93d-114">Requirement</span></span> | <span data-ttu-id="de93d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de93d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de93d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="de93d-116">Version</span></span><br/> | <span data-ttu-id="de93d-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="de93d-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="de93d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="de93d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="de93d-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de93d-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de93d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="de93d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de93d-121">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="de93d-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="de93d-122">**DownloadItem. Size**</span><span class="sxs-lookup"><span data-stu-id="de93d-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





