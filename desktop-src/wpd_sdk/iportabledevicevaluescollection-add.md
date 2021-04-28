---
description: 'Método IPortableDeviceValuesCollection:: Add – o método add adiciona um item à coleção.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Método IPortableDeviceValuesCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083234"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="05547-103">Método IPortableDeviceValuesCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="05547-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="05547-104">O método **Add** adiciona um item à coleção.</span><span class="sxs-lookup"><span data-stu-id="05547-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05547-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05547-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="05547-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05547-107">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05547-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05547-108">Ponteiro para uma interface **IPortableDeviceValues** para adicionar à coleção.</span><span class="sxs-lookup"><span data-stu-id="05547-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="05547-109">A interface não é realmente copiada, mas **AddRef** é chamado nela.</span><span class="sxs-lookup"><span data-stu-id="05547-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05547-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="05547-110">Return value</span></span>

<span data-ttu-id="05547-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="05547-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="05547-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="05547-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="05547-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="05547-113">Return code</span></span>                                                                                   | <span data-ttu-id="05547-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="05547-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05547-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05547-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05547-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="05547-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="05547-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05547-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05547-118">Não há memória suficiente disponível para adicionar o valor à coleção.</span><span class="sxs-lookup"><span data-stu-id="05547-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05547-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05547-119">Requirements</span></span>



| <span data-ttu-id="05547-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="05547-120">Requirement</span></span> | <span data-ttu-id="05547-121">Valor</span><span class="sxs-lookup"><span data-stu-id="05547-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05547-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05547-122">Header</span></span><br/>  | <dl> <span data-ttu-id="05547-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="05547-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="05547-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05547-124">Library</span></span><br/> | <dl> <span data-ttu-id="05547-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05547-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05547-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05547-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05547-127">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="05547-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




