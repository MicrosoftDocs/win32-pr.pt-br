---
description: O método getfloatvalue recupera um valor FLOAT (tipo VT \_ R4) especificado por uma chave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Método IPortableDeviceValues:: getfloatvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752139"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="610d4-103">Método IPortableDeviceValues:: getfloatvalue</span><span class="sxs-lookup"><span data-stu-id="610d4-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="610d4-104">O método **Getfloatvalue** recupera um valor **float** (tipo VT \_ R4) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="610d4-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="610d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="610d4-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="610d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="610d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610d4-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="610d4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610d4-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="610d4-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="610d4-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="610d4-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610d4-110">Ponteiro para o valor **float** recuperado.</span><span class="sxs-lookup"><span data-stu-id="610d4-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610d4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="610d4-111">Return value</span></span>

<span data-ttu-id="610d4-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="610d4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="610d4-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="610d4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="610d4-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="610d4-114">Return code</span></span>                                                                                             | <span data-ttu-id="610d4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="610d4-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="610d4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="610d4-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="610d4-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="610d4-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="610d4-119">A propriedade especificada pela *chave* não é um tipo **float** .</span><span class="sxs-lookup"><span data-stu-id="610d4-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="610d4-120"><dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="610d4-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="610d4-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="610d4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="610d4-122">Requirements</span></span>



| <span data-ttu-id="610d4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="610d4-123">Requirement</span></span> | <span data-ttu-id="610d4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="610d4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610d4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="610d4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="610d4-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="610d4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="610d4-127">Library</span></span><br/> | <dl> <span data-ttu-id="610d4-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610d4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="610d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610d4-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="610d4-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="610d4-131">**IPortableDeviceValues:: setfloatvalue**</span><span class="sxs-lookup"><span data-stu-id="610d4-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




