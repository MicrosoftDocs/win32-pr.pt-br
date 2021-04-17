---
title: DownloadCollection.id
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade ID recupera a ID da coleção de download.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759722"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="5b50b-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="5b50b-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="5b50b-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5b50b-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5b50b-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5b50b-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5b50b-109">A propriedade **ID** recupera a ID da coleção de download.</span><span class="sxs-lookup"><span data-stu-id="5b50b-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b50b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b50b-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="5b50b-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5b50b-111">Possible Values</span></span>

<span data-ttu-id="5b50b-112">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5b50b-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b50b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b50b-113">Remarks</span></span>

<span data-ttu-id="5b50b-114">Quando o Gerenciador de download cria uma nova coleção de download, ele atribui à coleção um número de ID.</span><span class="sxs-lookup"><span data-stu-id="5b50b-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="5b50b-115">Os números de ID persistem entre sessões do Windows Media Player e sessões do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5b50b-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="5b50b-116">Os números de ID não são exclusivos.</span><span class="sxs-lookup"><span data-stu-id="5b50b-116">ID numbers are not unique.</span></span> <span data-ttu-id="5b50b-117">No entanto, há números de ID suficientes disponíveis no valor de 32 bits que é extremamente improvável que um número de ID existente será substituído por um novo.</span><span class="sxs-lookup"><span data-stu-id="5b50b-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b50b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b50b-118">Requirements</span></span>



| <span data-ttu-id="5b50b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b50b-119">Requirement</span></span> | <span data-ttu-id="5b50b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5b50b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b50b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="5b50b-121">Version</span></span><br/> | <span data-ttu-id="5b50b-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5b50b-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5b50b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5b50b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b50b-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b50b-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b50b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b50b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b50b-126">**Objeto downloadcollection**</span><span class="sxs-lookup"><span data-stu-id="5b50b-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





