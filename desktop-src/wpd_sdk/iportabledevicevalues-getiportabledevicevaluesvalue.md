---
description: O método GetIPortableDeviceValuesValue recupera um valor de IPortableDeviceValues (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Método IPortableDeviceValues:: GetIPortableDeviceValuesValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749937"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="01908-103">Método IPortableDeviceValues:: GetIPortableDeviceValuesValue</span><span class="sxs-lookup"><span data-stu-id="01908-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="01908-104">O método **GetIPortableDeviceValuesValue** recupera um valor de **IPORTABLEDEVICEVALUES** (tipo VT \_ desconhecido) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="01908-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="01908-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01908-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="01908-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01908-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01908-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01908-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="01908-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="01908-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01908-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01908-110">Endereço de uma variável que recebe um ponteiro para a interface [**IPortableDeviceValues**](iportabledevicevalues.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="01908-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="01908-111">O chamador é responsável por chamar **Release** na interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="01908-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01908-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01908-112">Return value</span></span>

<span data-ttu-id="01908-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="01908-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="01908-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01908-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="01908-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01908-115">Return code</span></span>                                                                                                            | <span data-ttu-id="01908-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01908-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01908-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01908-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="01908-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="01908-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="01908-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="01908-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="01908-120">A propriedade especificada por *chave* não é uma interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="01908-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="01908-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="01908-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="01908-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="01908-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="01908-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01908-123">Examples</span></span>

<span data-ttu-id="01908-124">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="01908-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01908-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01908-125">Requirements</span></span>



| <span data-ttu-id="01908-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="01908-126">Requirement</span></span> | <span data-ttu-id="01908-127">Valor</span><span class="sxs-lookup"><span data-stu-id="01908-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01908-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01908-128">Header</span></span><br/>  | <dl> <span data-ttu-id="01908-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="01908-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="01908-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01908-130">Library</span></span><br/> | <dl> <span data-ttu-id="01908-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01908-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01908-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="01908-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01908-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="01908-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="01908-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="01908-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="01908-135">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="01908-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="01908-136">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="01908-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




