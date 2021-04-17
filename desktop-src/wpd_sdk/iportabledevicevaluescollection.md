---
description: A interface IPortableDeviceValuesCollection contém uma coleção de interfaces IPortableDeviceValues indexadas com base em zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interface IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808331"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="5eae4-103">Interface IPortableDeviceValuesCollection</span><span class="sxs-lookup"><span data-stu-id="5eae4-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="5eae4-104">A interface **IPortableDeviceValuesCollection** contém uma coleção de interfaces **IPortableDeviceValues** indexadas com base em zero.</span><span class="sxs-lookup"><span data-stu-id="5eae4-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="5eae4-105">Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceValuesCollection**.</span><span class="sxs-lookup"><span data-stu-id="5eae4-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="5eae4-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5eae4-106">Members</span></span>

<span data-ttu-id="5eae4-107">A interface **IPortableDeviceValuesCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5eae4-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5eae4-108">**IPortableDeviceValuesCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5eae4-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="5eae4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5eae4-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5eae4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5eae4-110">Methods</span></span>

<span data-ttu-id="5eae4-111">A interface **IPortableDeviceValuesCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5eae4-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="5eae4-112">Método</span><span class="sxs-lookup"><span data-stu-id="5eae4-112">Method</span></span>                                                       | <span data-ttu-id="5eae4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eae4-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eae4-114">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="5eae4-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="5eae4-115">Adiciona um item à coleção</span><span class="sxs-lookup"><span data-stu-id="5eae4-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="5eae4-116">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="5eae4-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="5eae4-117">Libera todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="5eae4-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="5eae4-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="5eae4-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="5eae4-119">Recupera um item da coleção por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="5eae4-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="5eae4-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="5eae4-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="5eae4-121">Recupera o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="5eae4-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="5eae4-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="5eae4-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="5eae4-123">Remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="5eae4-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5eae4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eae4-124">Requirements</span></span>



| <span data-ttu-id="5eae4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eae4-125">Requirement</span></span> | <span data-ttu-id="5eae4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5eae4-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eae4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5eae4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5eae4-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eae4-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5eae4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5eae4-129">Library</span></span><br/> | <dl> <span data-ttu-id="5eae4-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eae4-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eae4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eae4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eae4-132">**Interfaces de coleção**</span><span class="sxs-lookup"><span data-stu-id="5eae4-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

