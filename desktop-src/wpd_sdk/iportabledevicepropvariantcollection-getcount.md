---
description: O método GetCount recupera o número de itens nesta coleção.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Método IPortableDevicePropVariantCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793996"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="5c53a-103">Método IPortableDevicePropVariantCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="5c53a-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="5c53a-104">O método **GetCount** recupera o número de itens nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="5c53a-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c53a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c53a-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="5c53a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c53a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c53a-107">*pcElems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c53a-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c53a-108">Ponteiro para um **DWORD** que contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="5c53a-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c53a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c53a-109">Return value</span></span>

<span data-ttu-id="5c53a-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5c53a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c53a-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c53a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c53a-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5c53a-112">Return code</span></span>                                                                               | <span data-ttu-id="5c53a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c53a-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5c53a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c53a-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5c53a-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5c53a-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="5c53a-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5c53a-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5c53a-117">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5c53a-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5c53a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c53a-118">Examples</span></span>

<span data-ttu-id="5c53a-119">Para obter um exemplo de como usar esse método, consulte [recuperando as categorias funcionais com suporte de um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="5c53a-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c53a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c53a-120">Requirements</span></span>



| <span data-ttu-id="5c53a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c53a-121">Requirement</span></span> | <span data-ttu-id="5c53a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5c53a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c53a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c53a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5c53a-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c53a-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c53a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c53a-125">Library</span></span><br/> | <dl> <span data-ttu-id="5c53a-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c53a-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c53a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c53a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c53a-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="5c53a-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="5c53a-129">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="5c53a-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="5c53a-130">Recuperando formatos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="5c53a-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="5c53a-131">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="5c53a-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="5c53a-132">Recuperando as categorias funcionais com suporte de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="5c53a-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="5c53a-133">Definindo propriedades para vários objetos</span><span class="sxs-lookup"><span data-stu-id="5c53a-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




