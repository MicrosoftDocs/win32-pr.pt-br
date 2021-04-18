---
description: O método getiunknownvalue recupera um valor de interface IUnknown (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Método IPortableDeviceValues:: getiunknownvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793373"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="e0b1e-103">Método IPortableDeviceValues:: getiunknownvalue</span><span class="sxs-lookup"><span data-stu-id="e0b1e-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="e0b1e-104">O método **Getiunknownvalue** recupera um valor de interface **IUnknown** (tipo VT \_ desconhecido) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b1e-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="e0b1e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b1e-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0b1e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b1e-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e0b1e-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0b1e-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b1e-110">Endereço de uma variável que recebe um ponteiro para a interface **IUnknown** recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="e0b1e-111">O chamador é responsável por chamar **Release** na interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b1e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0b1e-112">Return value</span></span>

<span data-ttu-id="e0b1e-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e0b1e-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e0b1e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0b1e-115">Return code</span></span>                                                                                                            | <span data-ttu-id="e0b1e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0b1e-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0b1e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1e-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e0b1e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e0b1e-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1e-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e0b1e-120">A propriedade especificada pela *chave* não é uma interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e0b1e-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="e0b1e-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1e-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e0b1e-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="e0b1e-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="e0b1e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b1e-123">Requirements</span></span>



| <span data-ttu-id="e0b1e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b1e-124">Requirement</span></span> | <span data-ttu-id="e0b1e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b1e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b1e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0b1e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e0b1e-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1e-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0b1e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0b1e-128">Library</span></span><br/> | <dl> <span data-ttu-id="e0b1e-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1e-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b1e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0b1e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b1e-131">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e0b1e-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e0b1e-132">**IPortableDeviceValues:: setiunknownvalue**</span><span class="sxs-lookup"><span data-stu-id="e0b1e-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




