---
description: O método GetAt recupera um PROPERTYKEY da coleção por índice.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Método IPortableDeviceKeyCollection:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810895"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="2699a-103">Método IPortableDeviceKeyCollection:: GetAt</span><span class="sxs-lookup"><span data-stu-id="2699a-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="2699a-104">O método **GetAt** recupera um **PROPERTYKEY** da coleção por índice.</span><span class="sxs-lookup"><span data-stu-id="2699a-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2699a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2699a-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="2699a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2699a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2699a-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2699a-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2699a-108">**DWORD** que contém o índice da chave a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="2699a-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="2699a-109">*pKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2699a-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2699a-110">Ponteiro para um objeto **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="2699a-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2699a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2699a-111">Return value</span></span>

<span data-ttu-id="2699a-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2699a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2699a-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2699a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2699a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2699a-114">Return code</span></span>                                                                                  | <span data-ttu-id="2699a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2699a-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2699a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2699a-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2699a-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2699a-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="2699a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2699a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2699a-119">O índice passado estava fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="2699a-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="2699a-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2699a-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="2699a-121">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2699a-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="2699a-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2699a-122">Examples</span></span>

<span data-ttu-id="2699a-123">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="2699a-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2699a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2699a-124">Requirements</span></span>



| <span data-ttu-id="2699a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2699a-125">Requirement</span></span> | <span data-ttu-id="2699a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2699a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2699a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2699a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2699a-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2699a-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2699a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2699a-129">Library</span></span><br/> | <dl> <span data-ttu-id="2699a-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2699a-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2699a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2699a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2699a-132">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2699a-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="2699a-133">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="2699a-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="2699a-134">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="2699a-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




