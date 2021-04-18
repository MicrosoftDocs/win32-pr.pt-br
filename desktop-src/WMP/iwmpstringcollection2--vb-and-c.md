---
title: Interface IWMPStringCollection2 (VB e C) (WMP. h)
description: Fornece métodos que complementam a interface IWMPStringCollection.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB e C) interface do Windows Media Player
- IWMPStringCollection2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810713"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="032d0-105">Interface IWMPStringCollection2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="032d0-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="032d0-106">Fornece métodos que complementam a interface **IWMPStringCollection** .</span><span class="sxs-lookup"><span data-stu-id="032d0-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="032d0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="032d0-107">Members</span></span>

<span data-ttu-id="032d0-108">A interface **IWMPStringCollection2 (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="032d0-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="032d0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="032d0-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="032d0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="032d0-110">Methods</span></span>

<span data-ttu-id="032d0-111">A interface **IWMPStringCollection2 (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="032d0-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="032d0-112">Método</span><span class="sxs-lookup"><span data-stu-id="032d0-112">Method</span></span>                                                                                                                 | <span data-ttu-id="032d0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="032d0-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="032d0-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="032d0-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="032d0-115">Retorna o número de atributos associados ao índice do item da coleção de cadeia de caracteres especificado, ao nome do atributo e ao idioma.</span><span class="sxs-lookup"><span data-stu-id="032d0-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="032d0-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="032d0-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="032d0-117">Retorna a cadeia de caracteres correspondente ao nome e ao índice do item da coleção de cadeia de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="032d0-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="032d0-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="032d0-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="032d0-119">Retorna o valor correspondente ao índice, nome, idioma e índice de atributo do item da coleção de cadeia de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="032d0-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="032d0-120">**isidêntico**</span><span class="sxs-lookup"><span data-stu-id="032d0-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="032d0-121">Retorna um valor que indica se o objeto fornecido é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="032d0-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="032d0-122">Obtenha uma interface **IWMPStringCollection2** convertendo o valor retornado pelo método [**IWMPMediaCollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) .</span><span class="sxs-lookup"><span data-stu-id="032d0-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="032d0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032d0-123">Requirements</span></span>



| <span data-ttu-id="032d0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="032d0-124">Requirement</span></span> | <span data-ttu-id="032d0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="032d0-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="032d0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="032d0-126">Header</span></span><br/> | <dl> <span data-ttu-id="032d0-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="032d0-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032d0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="032d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032d0-129">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="032d0-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="032d0-130">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="032d0-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





