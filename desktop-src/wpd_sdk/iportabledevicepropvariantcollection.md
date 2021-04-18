---
description: A interface IPortableDevicePropVariantCollection contém uma coleção de valores PROPVARIANT indexados do mesmo VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interface IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793919"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="670fc-103">Interface IPortableDevicePropVariantCollection</span><span class="sxs-lookup"><span data-stu-id="670fc-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="670fc-104">A interface **IPortableDevicePropVariantCollection** contém uma coleção de valores **PROPVARIANT** indexados do mesmo VarType.</span><span class="sxs-lookup"><span data-stu-id="670fc-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="670fc-105">O VARTYPE do primeiro item que é adicionado à coleção determina o VARTYPE da coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="670fc-106">Uma tentativa de adicionar um item de um VARTYPE diferente poderá falhar se o valor de **PROPVARIANT** não puder ser alterado para o VarType atual da coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="670fc-107">Para alterar o VARTYPE da coleção, chame **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="670fc-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="670fc-108">Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDevicePropVariantCollection**.</span><span class="sxs-lookup"><span data-stu-id="670fc-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="670fc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="670fc-109">Members</span></span>

<span data-ttu-id="670fc-110">A interface **IPortableDevicePropVariantCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="670fc-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="670fc-111">**IPortableDevicePropVariantCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="670fc-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="670fc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="670fc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="670fc-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="670fc-113">Methods</span></span>

<span data-ttu-id="670fc-114">A interface **IPortableDevicePropVariantCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="670fc-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="670fc-115">Método</span><span class="sxs-lookup"><span data-stu-id="670fc-115">Method</span></span>                                                                | <span data-ttu-id="670fc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="670fc-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="670fc-117">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="670fc-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="670fc-118">Adiciona um item à coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="670fc-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="670fc-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="670fc-120">Converte todos os itens da coleção no VARTYPE especificado.</span><span class="sxs-lookup"><span data-stu-id="670fc-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="670fc-121">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="670fc-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="670fc-122">Libera e, em seguida, remove todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="670fc-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="670fc-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="670fc-124">Recupera um item da coleção por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="670fc-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="670fc-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="670fc-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="670fc-126">Recupera o número de itens nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="670fc-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="670fc-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="670fc-128">Recupera o tipo de dados dos itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="670fc-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="670fc-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="670fc-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="670fc-130">Remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="670fc-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="670fc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670fc-131">Requirements</span></span>



| <span data-ttu-id="670fc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="670fc-132">Requirement</span></span> | <span data-ttu-id="670fc-133">Valor</span><span class="sxs-lookup"><span data-stu-id="670fc-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670fc-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="670fc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="670fc-135"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="670fc-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="670fc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="670fc-136">Library</span></span><br/> | <dl> <span data-ttu-id="670fc-137"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="670fc-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670fc-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="670fc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670fc-139">**Interfaces de coleção**</span><span class="sxs-lookup"><span data-stu-id="670fc-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

