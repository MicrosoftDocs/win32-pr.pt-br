---
description: O método GetIPortableDeviceKeyCollectionValue recupera um valor de IPortableDeviceKeyCollection (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Método IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759578"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="9e510-103">Método IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue</span><span class="sxs-lookup"><span data-stu-id="9e510-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="9e510-104">O método **GetIPortableDeviceKeyCollectionValue** recupera um valor de **IPORTABLEDEVICEKEYCOLLECTION** (tipo VT \_ desconhecido) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="9e510-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e510-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e510-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="9e510-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e510-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e510-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e510-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9e510-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9e510-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e510-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e510-110">Ponteiro para o ponteiro de interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperado.</span><span class="sxs-lookup"><span data-stu-id="9e510-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="9e510-111">O chamador é responsável por chamar **Release** na interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="9e510-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e510-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e510-112">Return value</span></span>

<span data-ttu-id="9e510-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e510-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9e510-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e510-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9e510-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9e510-115">Return code</span></span>                                                                                                            | <span data-ttu-id="9e510-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e510-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e510-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e510-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="9e510-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9e510-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9e510-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="9e510-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="9e510-120">A propriedade especificada por *chave* não é uma interface **IPortableDeviceKeyCollection** .</span><span class="sxs-lookup"><span data-stu-id="9e510-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="9e510-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="9e510-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="9e510-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="9e510-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="9e510-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e510-123">Examples</span></span>

<span data-ttu-id="9e510-124">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="9e510-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e510-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e510-125">Requirements</span></span>



| <span data-ttu-id="9e510-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e510-126">Requirement</span></span> | <span data-ttu-id="9e510-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9e510-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e510-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e510-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9e510-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e510-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e510-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e510-130">Library</span></span><br/> | <dl> <span data-ttu-id="9e510-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e510-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e510-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e510-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e510-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="9e510-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9e510-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="9e510-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="9e510-135">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="9e510-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="9e510-136">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="9e510-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




