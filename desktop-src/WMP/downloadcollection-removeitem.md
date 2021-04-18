---
title: Método downloadcollection. removeItem
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método removeItem remove um item de download de uma coleção de download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- método removeItem Windows Media Player
- método removeItem Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758223"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="c815f-108">Método downloadcollection. removeItem</span><span class="sxs-lookup"><span data-stu-id="c815f-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="c815f-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="c815f-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c815f-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="c815f-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c815f-111">O método **RemoveItem** remove um item de download de uma coleção de download.</span><span class="sxs-lookup"><span data-stu-id="c815f-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c815f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c815f-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="c815f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c815f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c815f-114">*ItemId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c815f-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c815f-115">**Número** (**longo**) especificando o índice do **DownloadItem** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c815f-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c815f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c815f-116">Return value</span></span>

<span data-ttu-id="c815f-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c815f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c815f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c815f-118">Remarks</span></span>

<span data-ttu-id="c815f-119">Se o download representado por *ItemId* estiver em andamento, esse método cancelará o download.</span><span class="sxs-lookup"><span data-stu-id="c815f-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="c815f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c815f-120">Requirements</span></span>



| <span data-ttu-id="c815f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c815f-121">Requirement</span></span> | <span data-ttu-id="c815f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c815f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c815f-123">Versão</span><span class="sxs-lookup"><span data-stu-id="c815f-123">Version</span></span><br/> | <span data-ttu-id="c815f-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c815f-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="c815f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c815f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c815f-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c815f-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c815f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c815f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c815f-128">**Downloadcollection. Item**</span><span class="sxs-lookup"><span data-stu-id="c815f-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="c815f-129">**Objeto downloadcollection**</span><span class="sxs-lookup"><span data-stu-id="c815f-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





