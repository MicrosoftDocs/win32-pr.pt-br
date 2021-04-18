---
description: O método GetIPortableDeviceValuesCollectionValue recupera um valor de IPortableDeviceValuesCollection (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Método IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793223"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="147d0-103">Método IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue</span><span class="sxs-lookup"><span data-stu-id="147d0-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="147d0-104">O método **GetIPortableDeviceValuesCollectionValue** recupera um valor de **IPORTABLEDEVICEVALUESCOLLECTION** (tipo VT \_ desconhecido) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="147d0-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="147d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="147d0-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="147d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="147d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="147d0-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="147d0-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="147d0-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="147d0-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="147d0-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="147d0-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="147d0-110">Endereço de uma variável que recebe um ponteiro para a interface [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="147d0-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="147d0-111">O chamador é responsável por chamar **Release** na interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="147d0-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="147d0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="147d0-112">Return value</span></span>

<span data-ttu-id="147d0-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="147d0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="147d0-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="147d0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="147d0-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="147d0-115">Return code</span></span>                                                                                                            | <span data-ttu-id="147d0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="147d0-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="147d0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="147d0-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="147d0-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="147d0-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="147d0-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="147d0-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="147d0-120">A propriedade especificada por *chave* não é uma interface **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="147d0-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="147d0-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="147d0-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="147d0-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="147d0-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="147d0-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="147d0-123">Examples</span></span>

<span data-ttu-id="147d0-124">Para obter um exemplo de como usar esse método, consulte [recuperando os recursos de renderização suportados por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="147d0-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="147d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147d0-125">Requirements</span></span>



| <span data-ttu-id="147d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="147d0-126">Requirement</span></span> | <span data-ttu-id="147d0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="147d0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="147d0-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="147d0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="147d0-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="147d0-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="147d0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="147d0-130">Library</span></span><br/> | <dl> <span data-ttu-id="147d0-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="147d0-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147d0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="147d0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147d0-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="147d0-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="147d0-134">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="147d0-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="147d0-135">**SetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="147d0-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




