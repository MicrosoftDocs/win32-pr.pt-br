---
description: 'Método IPortableDevicePropVariantCollection:: GetAt – o método GetAt recupera um item da coleção por um índice baseado em zero.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Método IPortableDevicePropVariantCollection:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106794"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="0b366-103">Método IPortableDevicePropVariantCollection:: GetAt</span><span class="sxs-lookup"><span data-stu-id="0b366-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="0b366-104">O método **GetAt** recupera um item da coleção por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="0b366-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b366-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b366-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0b366-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b366-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b366-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b366-108">**DWORD** que contém o índice de base zero do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="0b366-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0b366-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0b366-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b366-110">Ponteiro para uma estrutura **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="0b366-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="0b366-111">O chamador é responsável por liberar essa memória chamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="0b366-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b366-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0b366-112">Return value</span></span>

<span data-ttu-id="0b366-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0b366-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b366-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b366-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b366-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0b366-115">Return code</span></span>                                                                                  | <span data-ttu-id="0b366-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b366-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="0b366-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b366-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0b366-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0b366-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="0b366-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="0b366-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="0b366-120">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0b366-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="0b366-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b366-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0b366-122">O índice que foi passado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="0b366-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0b366-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b366-123">Examples</span></span>

<span data-ttu-id="0b366-124">Para obter um exemplo de como usar esse método, consulte [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b366-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b366-125">Requirements</span></span>



| <span data-ttu-id="0b366-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b366-126">Requirement</span></span> | <span data-ttu-id="0b366-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0b366-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b366-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b366-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0b366-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b366-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b366-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b366-130">Library</span></span><br/> | <dl> <span data-ttu-id="0b366-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b366-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b366-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0b366-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b366-133">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="0b366-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="0b366-134">Recuperando um identificador de objeto de um identificador exclusivo persistente</span><span class="sxs-lookup"><span data-stu-id="0b366-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="0b366-135">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="0b366-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="0b366-136">Recuperando formatos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="0b366-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="0b366-137">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="0b366-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="0b366-138">Recuperando os tipos de conteúdo com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b366-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="0b366-139">Recuperando as categorias funcionais com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b366-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="0b366-140">Recuperando os identificadores de objeto funcional para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b366-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="0b366-141">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b366-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="0b366-142">Definindo propriedades para vários objetos</span><span class="sxs-lookup"><span data-stu-id="0b366-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




