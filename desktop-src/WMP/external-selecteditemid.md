---
title: External. selectedItemid
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. selectedItemid
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External. selectedItemid Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760065"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="77480-105">External. selectedItemid</span><span class="sxs-lookup"><span data-stu-id="77480-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="77480-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="77480-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="77480-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="77480-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="77480-108">A propriedade **selecteditemid** recupera o identificador do item de mídia selecionado no momento no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="77480-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="77480-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77480-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="77480-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="77480-110">Possible Values</span></span>

<span data-ttu-id="77480-111">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="77480-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77480-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="77480-112">Remarks</span></span>

<span data-ttu-id="77480-113">Essa propriedade é usada em combinação com a propriedade [external. selecteditemtype](external-selecteditemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="77480-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="77480-114">Por exemplo, se **selecteditemtype** for igual a CPTrackID, **selecteditemid** será a ID da faixa selecionada. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="77480-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="77480-115">Determinadas exibições no Windows Media Player têm um item de mídia específico selecionado.</span><span class="sxs-lookup"><span data-stu-id="77480-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="77480-116">Por exemplo, suponha que a exibição atual represente um álbum.</span><span class="sxs-lookup"><span data-stu-id="77480-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="77480-117">Um álbum é um contêiner de faixas, portanto **selecteditemtype** é igual a CPTrackID e **selecteditemid** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado.</span><span class="sxs-lookup"><span data-stu-id="77480-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="77480-118">Por exemplo, se o usuário clicar no nó raiz do armazenamento online no controle de exibição de árvore, o Windows Media Player exibirá uma página de descoberta fornecida pela loja online.</span><span class="sxs-lookup"><span data-stu-id="77480-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="77480-119">O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player.</span><span class="sxs-lookup"><span data-stu-id="77480-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="77480-120">Nesse caso, **selecteditemtype** é igual a UnknownLocation e **selecteditemid** é igual à cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="77480-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="77480-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77480-121">Requirements</span></span>



| <span data-ttu-id="77480-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="77480-122">Requirement</span></span> | <span data-ttu-id="77480-123">Valor</span><span class="sxs-lookup"><span data-stu-id="77480-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77480-124">Versão</span><span class="sxs-lookup"><span data-stu-id="77480-124">Version</span></span><br/> | <span data-ttu-id="77480-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="77480-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="77480-126">DLL</span><span class="sxs-lookup"><span data-stu-id="77480-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="77480-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77480-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77480-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="77480-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77480-129">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="77480-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="77480-130">**External. selectedItemtype**</span><span class="sxs-lookup"><span data-stu-id="77480-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="77480-131">**Local e item selecionado**</span><span class="sxs-lookup"><span data-stu-id="77480-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





