---
description: O método GetUnsignedLargeIntegerValue recupera um valor ULONGLONG (tipo VT \_ UI8) especificado por uma chave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Método IPortableDeviceValues:: GetUnsignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747273"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="aa4a7-103">Método IPortableDeviceValues:: GetUnsignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="aa4a7-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="aa4a7-104">O método **GetUnsignedLargeIntegerValue** recupera um valor **ULONGLONG** (tipo VT \_ UI8) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa4a7-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="aa4a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa4a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4a7-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa4a7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4a7-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="aa4a7-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa4a7-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4a7-110">Ponteiro para o valor **ULONGLONG** recuperado.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4a7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa4a7-111">Return value</span></span>

<span data-ttu-id="aa4a7-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aa4a7-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aa4a7-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aa4a7-114">Return code</span></span>                                                                                                            | <span data-ttu-id="aa4a7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa4a7-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa4a7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a7-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="aa4a7-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="aa4a7-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a7-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="aa4a7-119">A propriedade especificada por *chave* não é um tipo **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="aa4a7-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="aa4a7-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a7-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="aa4a7-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="aa4a7-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="aa4a7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4a7-122">Requirements</span></span>



| <span data-ttu-id="aa4a7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4a7-123">Requirement</span></span> | <span data-ttu-id="aa4a7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4a7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4a7-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa4a7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="aa4a7-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a7-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa4a7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa4a7-127">Library</span></span><br/> | <dl> <span data-ttu-id="aa4a7-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa4a7-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4a7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa4a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4a7-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="aa4a7-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="aa4a7-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="aa4a7-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




