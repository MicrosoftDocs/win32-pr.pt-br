---
description: O método add adiciona um item à coleção.
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
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807140"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="153a5-103">Método IPortableDeviceValuesCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="153a5-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="153a5-104">O método **Add** adiciona um item à coleção.</span><span class="sxs-lookup"><span data-stu-id="153a5-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="153a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="153a5-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="153a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="153a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153a5-107">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="153a5-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153a5-108">Ponteiro para uma interface **IPortableDeviceValues** para adicionar à coleção.</span><span class="sxs-lookup"><span data-stu-id="153a5-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="153a5-109">A interface não é realmente copiada, mas **AddRef** é chamado nela.</span><span class="sxs-lookup"><span data-stu-id="153a5-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153a5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="153a5-110">Return value</span></span>

<span data-ttu-id="153a5-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="153a5-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="153a5-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="153a5-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="153a5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="153a5-113">Return code</span></span>                                                                                   | <span data-ttu-id="153a5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="153a5-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="153a5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="153a5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="153a5-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="153a5-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="153a5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="153a5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="153a5-118">Não há memória suficiente disponível para adicionar o valor à coleção.</span><span class="sxs-lookup"><span data-stu-id="153a5-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="153a5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="153a5-119">Requirements</span></span>



| <span data-ttu-id="153a5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="153a5-120">Requirement</span></span> | <span data-ttu-id="153a5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="153a5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153a5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="153a5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="153a5-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="153a5-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="153a5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="153a5-124">Library</span></span><br/> | <dl> <span data-ttu-id="153a5-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="153a5-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153a5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="153a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153a5-127">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="153a5-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




