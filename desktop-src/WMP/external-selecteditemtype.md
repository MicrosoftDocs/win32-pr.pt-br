---
title: External. selectedItemtype
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. selectedItemtype
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External. selectedItemtype Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811102"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="670f1-105">External. selectedItemtype</span><span class="sxs-lookup"><span data-stu-id="670f1-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="670f1-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="670f1-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="670f1-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="670f1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="670f1-108">A propriedade **selecteditemtype** recupera o tipo do item de mídia selecionado no momento no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="670f1-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="670f1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="670f1-109">Syntax</span></span>

<span data-ttu-id="670f1-110">janela. external. selectedItemtype ()</span><span class="sxs-lookup"><span data-stu-id="670f1-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="670f1-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="670f1-111">Possible Values</span></span>

<span data-ttu-id="670f1-112">Essa propriedade é uma **cadeia de caracteres** somente leitura que contém uma das [constantes de localização da biblioteca](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="670f1-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="670f1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="670f1-113">Remarks</span></span>

<span data-ttu-id="670f1-114">Essa propriedade é usada em combinação com a propriedade **external. selecteditemid** .</span><span class="sxs-lookup"><span data-stu-id="670f1-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="670f1-115">Por exemplo, se **selecteditemtype** for igual a CPTrackID, **selecteditemid** será a ID da faixa selecionada. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="670f1-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="670f1-116">Determinadas exibições no Windows Media Player têm um item de mídia específico selecionado.</span><span class="sxs-lookup"><span data-stu-id="670f1-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="670f1-117">Por exemplo, suponha que a exibição atual represente um álbum.</span><span class="sxs-lookup"><span data-stu-id="670f1-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="670f1-118">Um álbum é um contêiner de faixas, portanto **selecteditemtype** é igual a CPTrackID e **selecteditemid** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado.</span><span class="sxs-lookup"><span data-stu-id="670f1-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="670f1-119">Por exemplo, se o usuário clicar no nó raiz do armazenamento online no controle de exibição de árvore, o Windows Media Player exibirá uma página de descoberta fornecida pela loja online.</span><span class="sxs-lookup"><span data-stu-id="670f1-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="670f1-120">O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player.</span><span class="sxs-lookup"><span data-stu-id="670f1-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="670f1-121">Nesse caso, **selecteditemtype** é igual a UnknownLocation e **selecteditemid** é igual à cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="670f1-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="670f1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670f1-122">Requirements</span></span>



| <span data-ttu-id="670f1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="670f1-123">Requirement</span></span> | <span data-ttu-id="670f1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="670f1-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="670f1-125">Versão</span><span class="sxs-lookup"><span data-stu-id="670f1-125">Version</span></span><br/> | <span data-ttu-id="670f1-126">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="670f1-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="670f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="670f1-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="670f1-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="670f1-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670f1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="670f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670f1-130">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="670f1-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="670f1-131">**External. selectedItemid**</span><span class="sxs-lookup"><span data-stu-id="670f1-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="670f1-132">**Local e item selecionado**</span><span class="sxs-lookup"><span data-stu-id="670f1-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





