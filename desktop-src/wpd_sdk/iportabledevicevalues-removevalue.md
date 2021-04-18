---
description: O método removervalue remove um item da coleção.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Método IPortableDeviceValues:: RemoveValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780403"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="17b9a-103">Método IPortableDeviceValues:: RemoveValue</span><span class="sxs-lookup"><span data-stu-id="17b9a-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="17b9a-104">O método **removervalue** remove um item da coleção.</span><span class="sxs-lookup"><span data-stu-id="17b9a-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b9a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b9a-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="17b9a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17b9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b9a-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17b9a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b9a-108">Um **REFPROPERTYKEY** que especifica o item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="17b9a-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b9a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17b9a-109">Return value</span></span>

<span data-ttu-id="17b9a-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="17b9a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17b9a-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="17b9a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="17b9a-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="17b9a-112">Return code</span></span>                                                                          | <span data-ttu-id="17b9a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="17b9a-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="17b9a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17b9a-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="17b9a-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="17b9a-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17b9a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b9a-116">Requirements</span></span>



| <span data-ttu-id="17b9a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b9a-117">Requirement</span></span> | <span data-ttu-id="17b9a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="17b9a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b9a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17b9a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="17b9a-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b9a-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="17b9a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17b9a-121">Library</span></span><br/> | <dl> <span data-ttu-id="17b9a-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17b9a-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b9a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="17b9a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b9a-124">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="17b9a-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="17b9a-125">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="17b9a-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="17b9a-126">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="17b9a-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




