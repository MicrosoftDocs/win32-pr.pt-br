---
title: Método downloadcollection. Item
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método item recupera um objeto de download pendente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método de item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810562"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="4669e-108">Método downloadcollection. Item</span><span class="sxs-lookup"><span data-stu-id="4669e-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="4669e-109">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="4669e-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4669e-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="4669e-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4669e-111">O método **Item** recupera um objeto de download pendente.</span><span class="sxs-lookup"><span data-stu-id="4669e-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4669e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4669e-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="4669e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4669e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4669e-114">*ItemId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4669e-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4669e-115">**Número** (**longo**) especificando o índice do **DownloadItem** a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="4669e-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4669e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4669e-116">Return value</span></span>

<span data-ttu-id="4669e-117">Esse método retorna um objeto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="4669e-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4669e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4669e-118">Remarks</span></span>

<span data-ttu-id="4669e-119">O valor de *ItemId* é baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="4669e-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="4669e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4669e-120">Requirements</span></span>



| <span data-ttu-id="4669e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4669e-121">Requirement</span></span> | <span data-ttu-id="4669e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4669e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4669e-123">Versão</span><span class="sxs-lookup"><span data-stu-id="4669e-123">Version</span></span><br/> | <span data-ttu-id="4669e-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4669e-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="4669e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4669e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4669e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4669e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4669e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4669e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4669e-128">**Objeto downloadcollection**</span><span class="sxs-lookup"><span data-stu-id="4669e-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="4669e-129">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="4669e-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





