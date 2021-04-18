---
title: Método external. Play
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método play instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- método play Windows Media Player
- método de reprodução Windows Media Player, classe externa
- Classe externa Windows Media Player, método play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783603"
---
# <a name="externalplay-method"></a><span data-ttu-id="06f25-108">Método external. Play</span><span class="sxs-lookup"><span data-stu-id="06f25-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="06f25-109">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="06f25-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="06f25-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="06f25-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="06f25-111">O método **Play** instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="06f25-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f25-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06f25-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="06f25-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06f25-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f25-114">*LibraryLocationType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06f25-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f25-115">Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo dos itens de mídia a serem reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="06f25-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="06f25-116">Por exemplo, CPAlbumID especifica que um ou mais álbuns devem ser reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="06f25-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="06f25-117">*LibraryLocationIDs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06f25-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f25-118">**Cadeia de caracteres** que contém os identificadores, delimitados por ponto e vírgula, dos itens de mídia a serem reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="06f25-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f25-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06f25-119">Return value</span></span>

<span data-ttu-id="06f25-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="06f25-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f25-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f25-121">Requirements</span></span>



| <span data-ttu-id="06f25-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f25-122">Requirement</span></span> | <span data-ttu-id="06f25-123">Valor</span><span class="sxs-lookup"><span data-stu-id="06f25-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06f25-124">Versão</span><span class="sxs-lookup"><span data-stu-id="06f25-124">Version</span></span><br/> | <span data-ttu-id="06f25-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="06f25-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="06f25-126">DLL</span><span class="sxs-lookup"><span data-stu-id="06f25-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="06f25-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06f25-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f25-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="06f25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f25-129">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="06f25-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





