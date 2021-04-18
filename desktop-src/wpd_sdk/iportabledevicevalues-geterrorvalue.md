---
description: O método geterrovalue recupera um valor HRESULT (erro de tipo VT \_ ) especificado por uma chave.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'Método IPortableDeviceValues:: geterrovalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752140"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="cc0f5-103">Método IPortableDeviceValues:: geterrovalue</span><span class="sxs-lookup"><span data-stu-id="cc0f5-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="cc0f5-104">O método **Geterrovalue** recupera um valor **HRESULT** (erro de tipo VT \_ ) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc0f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc0f5-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="cc0f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc0f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc0f5-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc0f5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0f5-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cc0f5-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc0f5-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0f5-110">Ponteiro para o valor **HRESULT** recuperado.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc0f5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc0f5-111">Return value</span></span>

<span data-ttu-id="cc0f5-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cc0f5-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cc0f5-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc0f5-114">Return code</span></span>                                                                                                            | <span data-ttu-id="cc0f5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc0f5-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc0f5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc0f5-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="cc0f5-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cc0f5-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="cc0f5-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="cc0f5-119">A propriedade especificada pela *chave* não é um tipo **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc0f5-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="cc0f5-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="cc0f5-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="cc0f5-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="cc0f5-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="cc0f5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc0f5-122">Requirements</span></span>



| <span data-ttu-id="cc0f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc0f5-123">Requirement</span></span> | <span data-ttu-id="cc0f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cc0f5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0f5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc0f5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cc0f5-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc0f5-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc0f5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc0f5-127">Library</span></span><br/> | <dl> <span data-ttu-id="cc0f5-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc0f5-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc0f5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc0f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0f5-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="cc0f5-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="cc0f5-131">**IPortableDeviceValues:: SetError**</span><span class="sxs-lookup"><span data-stu-id="cc0f5-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




