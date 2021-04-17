---
title: Método external. addToBasket
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. addToBasket
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- método addToBasket Windows Media Player
- método addToBasket Windows Media Player, classe externa
- Classe externa Windows Media Player, método addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759707"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="2d2b8-107">Método external. addToBasket</span><span class="sxs-lookup"><span data-stu-id="2d2b8-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="2d2b8-108">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2d2b8-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2d2b8-110">O método **addToBasket** adiciona itens de mídia ao painel de lista (também chamado de cesta) no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2b8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d2b8-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="2d2b8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d2b8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d2b8-113">*Modo de exibição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d2b8-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d2b8-114">**Cadeia de caracteres** que especifica o tipo de item que está sendo adicionado ao painel de lista.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="2d2b8-115">O chamador deve definir esse parâmetro como uma das seguintes [constantes de localização de biblioteca](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="2d2b8-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="2d2b8-116">CPListID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-116">CPListID</span></span>

<span data-ttu-id="2d2b8-117">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-117">CPTrackID</span></span>

<span data-ttu-id="2d2b8-118">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-118">CPAlbumID</span></span>

<span data-ttu-id="2d2b8-119">CPArtist</span><span class="sxs-lookup"><span data-stu-id="2d2b8-119">CPArtist</span></span>

<span data-ttu-id="2d2b8-120">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-120">CPGenreID</span></span>

<span data-ttu-id="2d2b8-121">CPAlbumSubGenreID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="2d2b8-122">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="2d2b8-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="2d2b8-123">*ViewIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d2b8-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d2b8-124">**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens a serem adicionados ao painel de lista.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d2b8-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d2b8-125">Return value</span></span>

<span data-ttu-id="2d2b8-126">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2b8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d2b8-127">Requirements</span></span>



| <span data-ttu-id="2d2b8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2b8-128">Requirement</span></span> | <span data-ttu-id="2d2b8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2d2b8-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2b8-130">Versão</span><span class="sxs-lookup"><span data-stu-id="2d2b8-130">Version</span></span><br/> | <span data-ttu-id="2d2b8-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="2d2b8-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="2d2b8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2b8-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d2b8-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d2b8-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d2b8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d2b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2b8-135">**Externalobject para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="2d2b8-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2d2b8-136">**External. basketTitle**</span><span class="sxs-lookup"><span data-stu-id="2d2b8-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





