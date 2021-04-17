---
title: External. libraryLocationType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Windows Media Player externo. libraryLocationType
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770490"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="71dc2-105">External. libraryLocationType</span><span class="sxs-lookup"><span data-stu-id="71dc2-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="71dc2-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="71dc2-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="71dc2-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="71dc2-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="71dc2-108">A propriedade **libraryLocationType** recupera uma [constante de local de biblioteca](library-location-constants.md) que indica o tipo da exibição atual no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="71dc2-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="71dc2-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="71dc2-109">Possible Values</span></span>

<span data-ttu-id="71dc2-110">Essa propriedade é uma **cadeia de caracteres** somente leitura que contém uma das constantes de localização da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="71dc2-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="71dc2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="71dc2-111">Remarks</span></span>

<span data-ttu-id="71dc2-112">Essa propriedade funciona em combinação com a propriedade [external. libraryLocationID](external-librarylocationid.md) .</span><span class="sxs-lookup"><span data-stu-id="71dc2-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="71dc2-113">Por exemplo, suponha que **libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3.</span><span class="sxs-lookup"><span data-stu-id="71dc2-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="71dc2-114">Isso significa que a exibição atual no Windows Media Player está mostrando o álbum que tem uma ID de 3.</span><span class="sxs-lookup"><span data-stu-id="71dc2-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="71dc2-115">Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="71dc2-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71dc2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71dc2-116">Requirements</span></span>



| <span data-ttu-id="71dc2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71dc2-117">Requirement</span></span> | <span data-ttu-id="71dc2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="71dc2-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71dc2-119">Versão</span><span class="sxs-lookup"><span data-stu-id="71dc2-119">Version</span></span><br/> | <span data-ttu-id="71dc2-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="71dc2-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="71dc2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="71dc2-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="71dc2-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71dc2-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71dc2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="71dc2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dc2-124">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="71dc2-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="71dc2-125">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="71dc2-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="71dc2-126">**Local e item selecionado**</span><span class="sxs-lookup"><span data-stu-id="71dc2-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





