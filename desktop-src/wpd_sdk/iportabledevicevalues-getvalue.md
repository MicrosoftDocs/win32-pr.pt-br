---
description: O método GetValue recupera um valor de PROPVARIANT especificado por uma chave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Método IPortableDeviceValues:: GetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764203"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="2be13-103">Método IPortableDeviceValues:: GetValue</span><span class="sxs-lookup"><span data-stu-id="2be13-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="2be13-104">O método **GetValue** recupera um valor de **PROPVARIANT** especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="2be13-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be13-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2be13-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="2be13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2be13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be13-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2be13-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be13-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="2be13-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2be13-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2be13-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2be13-110">Ponteiro para o valor **PROPVARIANT** recuperado.</span><span class="sxs-lookup"><span data-stu-id="2be13-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="2be13-111">O chamador deve liberar a memória chamando **PropVariantClear** quando terminar com ela.</span><span class="sxs-lookup"><span data-stu-id="2be13-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be13-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2be13-112">Return value</span></span>

<span data-ttu-id="2be13-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2be13-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2be13-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2be13-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2be13-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2be13-115">Return code</span></span>                                                                                                            | <span data-ttu-id="2be13-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2be13-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="2be13-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2be13-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="2be13-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2be13-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2be13-119"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="2be13-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="2be13-120">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="2be13-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2be13-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2be13-121">Remarks</span></span>

<span data-ttu-id="2be13-122">Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para a recuperação de um buffer de tamanho **nulo ou NULL** .</span><span class="sxs-lookup"><span data-stu-id="2be13-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="2be13-123">Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2be13-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="2be13-124">Esse método pode ser usado para recuperar um valor de qualquer tipo da coleção.</span><span class="sxs-lookup"><span data-stu-id="2be13-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="2be13-125">No entanto, se você souber o tipo de valor com antecedência, use um dos métodos de recuperação especializados dessa interface para evitar a sobrecarga de trabalhar diretamente com valores de PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="2be13-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be13-126">Requirements</span></span>



| <span data-ttu-id="2be13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be13-127">Requirement</span></span> | <span data-ttu-id="2be13-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2be13-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be13-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2be13-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2be13-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be13-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2be13-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be13-131">Library</span></span><br/> | <dl> <span data-ttu-id="2be13-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2be13-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be13-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2be13-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be13-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="2be13-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2be13-135">**IPortableDeviceValues:: RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="2be13-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="2be13-136">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="2be13-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




