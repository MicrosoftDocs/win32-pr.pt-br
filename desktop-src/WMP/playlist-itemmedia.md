---
title: PLAYLIST. @ Media
description: O atributo de mídia recupera o objeto de mídia correspondente ao índice fornecido no elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST. multimídia do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755710"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="9a588-104">PLAYLIST. @ Media</span><span class="sxs-lookup"><span data-stu-id="9a588-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="9a588-105">O atributo de **mídia** recupera o objeto de **mídia** correspondente ao índice fornecido no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="9a588-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="9a588-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9a588-106">Possible Values</span></span>

<span data-ttu-id="9a588-107">Esse atributo é um objeto de **mídia** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9a588-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a588-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a588-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a588-109"><span id="index"></span><span id="INDEX"></span>*index*</span><span class="sxs-lookup"><span data-stu-id="9a588-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="9a588-110">**Número**(**longo**) que contém o índice de um item da playlist.</span><span class="sxs-lookup"><span data-stu-id="9a588-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a588-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a588-111">Remarks</span></span>

<span data-ttu-id="9a588-112">A **Propriedade do ItemProperty retornará os objetos** de mídia que são expandidos no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="9a588-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="9a588-113">Por exemplo, se houver uma lista de reprodução que contenha três clipes de mídia que não esteja expandido no elemento **playlist** , o de **mídia**(0) retornará a playlist como o objeto de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a588-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="9a588-114">Se a lista de reprodução for expandida, o **arquivo** de mídia (0) retornará o primeiro clipe de mídia na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="9a588-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a588-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a588-115">Requirements</span></span>



| <span data-ttu-id="9a588-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a588-116">Requirement</span></span> | <span data-ttu-id="9a588-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9a588-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9a588-118">Versão</span><span class="sxs-lookup"><span data-stu-id="9a588-118">Version</span></span><br/> | <span data-ttu-id="9a588-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9a588-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a588-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a588-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a588-121">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="9a588-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9a588-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9a588-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





