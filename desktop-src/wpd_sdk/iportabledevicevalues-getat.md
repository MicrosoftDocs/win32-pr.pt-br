---
description: O método GetAt recupera um valor da coleção usando o índice de base zero fornecido.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Método IPortableDeviceValues:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747651"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="3730c-103">Método IPortableDeviceValues:: GetAt</span><span class="sxs-lookup"><span data-stu-id="3730c-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="3730c-104">O método **GetAt** recupera um valor da coleção usando o índice de base zero fornecido.</span><span class="sxs-lookup"><span data-stu-id="3730c-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3730c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3730c-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3730c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3730c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3730c-107">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3730c-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3730c-108">Um **DWORD** que especifica um índice de base zero na coleção.</span><span class="sxs-lookup"><span data-stu-id="3730c-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3730c-109">*pKey* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3730c-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3730c-110">Um ponteiro de **PROPERTYKEY** opcional que recupera a chave do item especificado.</span><span class="sxs-lookup"><span data-stu-id="3730c-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="3730c-111">*valores* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3730c-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3730c-112">Um **PROPVARIANT** opcional que recupera o valor do item especificado.</span><span class="sxs-lookup"><span data-stu-id="3730c-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="3730c-113">O chamador deve liberar a memória chamando **PropVariantClear** quando terminar com ela.</span><span class="sxs-lookup"><span data-stu-id="3730c-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3730c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3730c-114">Return value</span></span>

<span data-ttu-id="3730c-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3730c-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3730c-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3730c-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3730c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3730c-117">Return code</span></span>                                                                                  | <span data-ttu-id="3730c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3730c-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="3730c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3730c-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3730c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3730c-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="3730c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3730c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3730c-122">Um número de índice inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="3730c-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3730c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3730c-123">Remarks</span></span>

<span data-ttu-id="3730c-124">Se uma propriedade indicar um valor do tipo VT \_ desconhecido, a propriedade será um dos dispositivos portáteis do Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) ou [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="3730c-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="3730c-125">Nenhuma outra interface pode ser retornada por dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="3730c-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="3730c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3730c-126">Requirements</span></span>



| <span data-ttu-id="3730c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3730c-127">Requirement</span></span> | <span data-ttu-id="3730c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3730c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3730c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3730c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3730c-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3730c-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3730c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3730c-131">Library</span></span><br/> | <dl> <span data-ttu-id="3730c-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3730c-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3730c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3730c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3730c-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3730c-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3730c-135">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="3730c-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




