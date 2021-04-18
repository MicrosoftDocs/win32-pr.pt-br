---
description: O método GetIPortableDevicePropVariantCollectionValue recupera um valor de IPortableDevicePropVariantCollection (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Método IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765662"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="861ec-103">Método IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue</span><span class="sxs-lookup"><span data-stu-id="861ec-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="861ec-104">O método **GetIPortableDevicePropVariantCollectionValue** recupera um valor de **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (tipo VT \_ desconhecido) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="861ec-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="861ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="861ec-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="861ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="861ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861ec-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="861ec-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="861ec-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="861ec-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="861ec-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="861ec-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="861ec-110">Endereço de uma variável que recebe um ponteiro para a interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperada.</span><span class="sxs-lookup"><span data-stu-id="861ec-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="861ec-111">O chamador é responsável por chamar **Release** na interface recuperada.</span><span class="sxs-lookup"><span data-stu-id="861ec-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="861ec-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="861ec-112">Return value</span></span>

<span data-ttu-id="861ec-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="861ec-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="861ec-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="861ec-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="861ec-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="861ec-115">Return code</span></span>                                                                                                            | <span data-ttu-id="861ec-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="861ec-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="861ec-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="861ec-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="861ec-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="861ec-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="861ec-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="861ec-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="861ec-120">A propriedade especificada por *chave* não é uma interface **IPortableDevicePropVariantCollection** .</span><span class="sxs-lookup"><span data-stu-id="861ec-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="861ec-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="861ec-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="861ec-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="861ec-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="861ec-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861ec-123">Requirements</span></span>



| <span data-ttu-id="861ec-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="861ec-124">Requirement</span></span> | <span data-ttu-id="861ec-125">Valor</span><span class="sxs-lookup"><span data-stu-id="861ec-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="861ec-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="861ec-126">Header</span></span><br/>  | <dl> <span data-ttu-id="861ec-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="861ec-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="861ec-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="861ec-128">Library</span></span><br/> | <dl> <span data-ttu-id="861ec-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="861ec-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="861ec-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="861ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861ec-131">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="861ec-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="861ec-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="861ec-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




