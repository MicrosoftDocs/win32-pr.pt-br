---
title: Método external. compre
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Buy inicia a compra de um conjunto de itens de mídia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- método de compra Windows Media Player
- método de compra Windows Media Player, classe externa
- Classe externa Windows Media Player, método de compra
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762072"
---
# <a name="externalbuy-method"></a><span data-ttu-id="f8a86-108">Método external. compre</span><span class="sxs-lookup"><span data-stu-id="f8a86-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="f8a86-109">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="f8a86-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f8a86-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="f8a86-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f8a86-111">O método **Buy** inicia a compra de um conjunto de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="f8a86-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a86-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8a86-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="f8a86-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8a86-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a86-114">*Modo de exibição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8a86-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a86-115">**Cadeia de caracteres** que especifica o tipo de item a ser comprado.</span><span class="sxs-lookup"><span data-stu-id="f8a86-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="f8a86-116">O chamador deve definir esse parâmetro como uma das seguintes [constantes de localização de biblioteca](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="f8a86-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="f8a86-117">CPListID</span><span class="sxs-lookup"><span data-stu-id="f8a86-117">CPListID</span></span>

<span data-ttu-id="f8a86-118">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="f8a86-118">CPTrackID</span></span>

<span data-ttu-id="f8a86-119">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="f8a86-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="f8a86-120">*ViewIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8a86-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a86-121">**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens a serem comprados.</span><span class="sxs-lookup"><span data-stu-id="f8a86-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a86-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8a86-122">Return value</span></span>

<span data-ttu-id="f8a86-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f8a86-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a86-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a86-124">Requirements</span></span>



| <span data-ttu-id="f8a86-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a86-125">Requirement</span></span> | <span data-ttu-id="f8a86-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a86-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a86-127">Versão</span><span class="sxs-lookup"><span data-stu-id="f8a86-127">Version</span></span><br/> | <span data-ttu-id="f8a86-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f8a86-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f8a86-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a86-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8a86-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8a86-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a86-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a86-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a86-132">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f8a86-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f8a86-133">**Externo. download**</span><span class="sxs-lookup"><span data-stu-id="f8a86-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="f8a86-134">**IWMPContentPartner:: comprar**</span><span class="sxs-lookup"><span data-stu-id="f8a86-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="f8a86-135">**Comprando conteúdo de mídia**</span><span class="sxs-lookup"><span data-stu-id="f8a86-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





