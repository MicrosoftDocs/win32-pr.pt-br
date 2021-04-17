---
title: Atributo albumid
description: O atributo albumid é um identificador exclusivo para o álbum.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Atributo albumid do Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783639"
---
# <a name="albumid-attribute"></a><span data-ttu-id="b1287-104">Atributo albumid</span><span class="sxs-lookup"><span data-stu-id="b1287-104">AlbumID Attribute</span></span>

<span data-ttu-id="b1287-105">O atributo **albumid** é um identificador exclusivo para o álbum.</span><span class="sxs-lookup"><span data-stu-id="b1287-105">The **AlbumID** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b1287-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="b1287-106">Applies To</span></span>

-   [<span data-ttu-id="b1287-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="b1287-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b1287-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1287-108">Remarks</span></span>

<span data-ttu-id="b1287-109">Esse atributo é armazenado somente na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="b1287-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="b1287-110">O identificador exclusivo é uma combinação do título do álbum e do nome do artista do álbum.</span><span class="sxs-lookup"><span data-stu-id="b1287-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="b1287-111">Nesse atributo, o título do álbum é exibido primeiro.</span><span class="sxs-lookup"><span data-stu-id="b1287-111">In this attribute, the album title comes first.</span></span> <span data-ttu-id="b1287-112">Quando você usa o método [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obter um objeto **StringCollection** usando esse atributo, os valores são classificados por título de álbum.</span><span class="sxs-lookup"><span data-stu-id="b1287-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album title.</span></span>

<span data-ttu-id="b1287-113">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b1287-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1287-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1287-114">Requirements</span></span>



| <span data-ttu-id="b1287-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1287-115">Requirement</span></span> | <span data-ttu-id="b1287-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b1287-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b1287-117">Versão</span><span class="sxs-lookup"><span data-stu-id="b1287-117">Version</span></span><br/> | <span data-ttu-id="b1287-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b1287-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1287-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1287-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1287-120">**Atributo AlbumIDAlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="b1287-120">**AlbumIDAlbumArtist Attribute**</span></span>](albumidalbumartist-attribute.md)
</dt> <dt>

[<span data-ttu-id="b1287-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="b1287-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





