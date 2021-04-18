---
description: A interface IPortableDeviceKeyCollection contém uma coleção de valores PROPERTYKEY. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame CoCreate com CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interface IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791490"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="4be5a-104">Interface IPortableDeviceKeyCollection</span><span class="sxs-lookup"><span data-stu-id="4be5a-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="4be5a-105">A interface **IPortableDeviceKeyCollection** contém uma coleção de valores **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="4be5a-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="4be5a-106">Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceKeyCollection**.</span><span class="sxs-lookup"><span data-stu-id="4be5a-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="4be5a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4be5a-107">Members</span></span>

<span data-ttu-id="4be5a-108">A interface **IPortableDeviceKeyCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4be5a-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4be5a-109">**IPortableDeviceKeyCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4be5a-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="4be5a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4be5a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4be5a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4be5a-111">Methods</span></span>

<span data-ttu-id="4be5a-112">A interface **IPortableDeviceKeyCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4be5a-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="4be5a-113">Método</span><span class="sxs-lookup"><span data-stu-id="4be5a-113">Method</span></span>                                                    | <span data-ttu-id="4be5a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4be5a-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="4be5a-115">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="4be5a-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="4be5a-116">Adiciona uma chave de propriedade à coleção.</span><span class="sxs-lookup"><span data-stu-id="4be5a-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="4be5a-117">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="4be5a-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="4be5a-118">Exclui todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="4be5a-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="4be5a-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="4be5a-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="4be5a-120">Recupera um **PROPERTYKEY** da coleção por índice.</span><span class="sxs-lookup"><span data-stu-id="4be5a-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="4be5a-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4be5a-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="4be5a-122">Recupera o número de chaves nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="4be5a-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="4be5a-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="4be5a-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="4be5a-124">Remove o elemento armazenado no local especificado pelo índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="4be5a-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4be5a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be5a-125">Requirements</span></span>



| <span data-ttu-id="4be5a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be5a-126">Requirement</span></span> | <span data-ttu-id="4be5a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4be5a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be5a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4be5a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4be5a-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be5a-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4be5a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4be5a-130">Library</span></span><br/> | <dl> <span data-ttu-id="4be5a-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4be5a-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be5a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4be5a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be5a-133">**Interfaces de coleção**</span><span class="sxs-lookup"><span data-stu-id="4be5a-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

