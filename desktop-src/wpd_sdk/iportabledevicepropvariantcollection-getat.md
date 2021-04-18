---
description: O método GetAt recupera um item da coleção por um índice baseado em zero.
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
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764305"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="3a05e-103">Método IPortableDevicePropVariantCollection:: GetAt</span><span class="sxs-lookup"><span data-stu-id="3a05e-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="3a05e-104">O método **GetAt** recupera um item da coleção por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="3a05e-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a05e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a05e-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3a05e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a05e-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a05e-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a05e-108">**DWORD** que contém o índice de base zero do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3a05e-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3a05e-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a05e-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a05e-110">Ponteiro para uma estrutura **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="3a05e-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="3a05e-111">O chamador é responsável por liberar essa memória chamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="3a05e-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a05e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a05e-112">Return value</span></span>

<span data-ttu-id="3a05e-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3a05e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a05e-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3a05e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a05e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3a05e-115">Return code</span></span>                                                                                  | <span data-ttu-id="3a05e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a05e-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="3a05e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a05e-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3a05e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3a05e-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="3a05e-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a05e-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3a05e-120">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3a05e-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="3a05e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3a05e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3a05e-122">O índice que foi passado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="3a05e-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="3a05e-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a05e-123">Examples</span></span>

<span data-ttu-id="3a05e-124">Para obter um exemplo de como usar esse método, consulte [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="3a05e-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a05e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a05e-125">Requirements</span></span>



| <span data-ttu-id="3a05e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a05e-126">Requirement</span></span> | <span data-ttu-id="3a05e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a05e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a05e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a05e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3a05e-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a05e-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a05e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a05e-130">Library</span></span><br/> | <dl> <span data-ttu-id="3a05e-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a05e-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a05e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a05e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a05e-133">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="3a05e-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="3a05e-134">Recuperando um identificador de objeto de um identificador exclusivo persistente</span><span class="sxs-lookup"><span data-stu-id="3a05e-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="3a05e-135">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="3a05e-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="3a05e-136">Recuperando formatos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="3a05e-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="3a05e-137">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="3a05e-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="3a05e-138">Recuperando os tipos de conteúdo com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a05e-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="3a05e-139">Recuperando as categorias funcionais com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a05e-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="3a05e-140">Recuperando os identificadores de objeto funcional para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a05e-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="3a05e-141">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a05e-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="3a05e-142">Definindo propriedades para vários objetos</span><span class="sxs-lookup"><span data-stu-id="3a05e-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




