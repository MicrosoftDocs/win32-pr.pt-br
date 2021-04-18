---
title: External. libraryLocationID
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Windows Media Player externo. libraryLocationID
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761445"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="356c2-105">External. libraryLocationID</span><span class="sxs-lookup"><span data-stu-id="356c2-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="356c2-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="356c2-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="356c2-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="356c2-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="356c2-108">A propriedade **libraryLocationID** recupera o identificador do item de mídia específico que é exibido atualmente no modo de exibição do Player.</span><span class="sxs-lookup"><span data-stu-id="356c2-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="356c2-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="356c2-109">Possible Values</span></span>

<span data-ttu-id="356c2-110">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="356c2-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="356c2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="356c2-111">Remarks</span></span>

<span data-ttu-id="356c2-112">Essa propriedade funciona em combinação com a propriedade [external. libraryLocationType](external-librarylocationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="356c2-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="356c2-113">Por exemplo, suponha que **libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3.</span><span class="sxs-lookup"><span data-stu-id="356c2-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="356c2-114">Isso significa que a exibição atual no Windows Media Player está mostrando o álbum que tem uma ID de 3.</span><span class="sxs-lookup"><span data-stu-id="356c2-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="356c2-115">Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="356c2-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="356c2-116">Determinadas exibições no Windows Media Player estão associadas a um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="356c2-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="356c2-117">Por exemplo, se a exibição atual representar um álbum individual, **libraryLocationType** será igual a CPAlbumID e **LIBRARYLOCATIONID** será a ID do álbum.</span><span class="sxs-lookup"><span data-stu-id="356c2-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="356c2-118">Outras exibições não estão associadas a nenhum item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="356c2-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="356c2-119">Por exemplo, se a exibição atual representar todos os álbuns, **libraryLocationType** será igual a AllCPAlbumIDs, mas não haverá nenhum valor significativo que possa ser atribuído a **libraryLocationID**.</span><span class="sxs-lookup"><span data-stu-id="356c2-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="356c2-120">Nos casos em que a propriedade **libraryLocationID** não tem nenhum valor significativo, ela é igual à cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="356c2-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="356c2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="356c2-121">Requirements</span></span>



| <span data-ttu-id="356c2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="356c2-122">Requirement</span></span> | <span data-ttu-id="356c2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="356c2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="356c2-124">Versão</span><span class="sxs-lookup"><span data-stu-id="356c2-124">Version</span></span><br/> | <span data-ttu-id="356c2-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="356c2-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="356c2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="356c2-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="356c2-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="356c2-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="356c2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="356c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="356c2-129">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="356c2-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="356c2-130">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="356c2-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="356c2-131">**Local e item selecionado**</span><span class="sxs-lookup"><span data-stu-id="356c2-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





