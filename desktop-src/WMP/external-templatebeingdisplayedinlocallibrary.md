---
title: External. templateBeingDisplayedInLocalLibrary
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Windows Media Player externo. templateBeingDisplayedInLocalLibrary
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758200"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="e8bdb-105">External. templateBeingDisplayedInLocalLibrary</span><span class="sxs-lookup"><span data-stu-id="e8bdb-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="e8bdb-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e8bdb-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e8bdb-108">A propriedade **templateBeingDisplayedInLocalLibrary** indica se o feed representado pela página de descoberta atual está sendo exibido no controle de exibição de árvore de biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bdb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8bdb-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="e8bdb-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e8bdb-110">Possible Values</span></span>

<span data-ttu-id="e8bdb-111">Esta propriedade é um **booliano** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="e8bdb-112">**Verdadeiro** indica que o feed está sendo exibido no controle de exibição de árvore de biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8bdb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8bdb-113">Remarks</span></span>

<span data-ttu-id="e8bdb-114">Uma página de descoberta que representa um feed para uma lista de reprodução dinâmica pode exibir um botão que permite ao usuário "salvar" o feed em sua biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="e8bdb-115">Salvar o feed, neste contexto, significa que alguns metadados são salvos no computador do usuário e o feed é listado no nó **playlists** no controle de exibição de árvore de biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="e8bdb-116">O script na página descoberta pode inspecionar a propriedade **templateBeingDisplayedInLocalLibrary** para determinar se o usuário já salvou o feed na biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="e8bdb-117">Se o usuário já tiver salvo o feed, a página de descoberta não deverá exibir o botão salvar.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="e8bdb-118">Uma página de descoberta que representa um feed de rádio deve inspecionar a propriedade **templateBeingDisplayedInLocalLibrary** pelo mesmo motivo.</span><span class="sxs-lookup"><span data-stu-id="e8bdb-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bdb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8bdb-119">Requirements</span></span>



| <span data-ttu-id="e8bdb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8bdb-120">Requirement</span></span> | <span data-ttu-id="e8bdb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8bdb-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bdb-122">Versão</span><span class="sxs-lookup"><span data-stu-id="e8bdb-122">Version</span></span><br/> | <span data-ttu-id="e8bdb-123">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="e8bdb-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="e8bdb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bdb-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8bdb-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bdb-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8bdb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8bdb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bdb-127">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e8bdb-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





