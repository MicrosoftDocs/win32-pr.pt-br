---
description: O método GetStringValue recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Método IPortableDeviceValues:: GetStringValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813478"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="e4145-103">Método IPortableDeviceValues:: GetStringValue</span><span class="sxs-lookup"><span data-stu-id="e4145-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="e4145-104">O método **GetStringValue** recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="e4145-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4145-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4145-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e4145-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4145-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4145-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4145-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e4145-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e4145-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4145-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4145-110">Ponteiro para o valor de **LPWSTR** recuperado.</span><span class="sxs-lookup"><span data-stu-id="e4145-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="e4145-111">O chamador é responsável por chamar **CoTaskMemFree** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="e4145-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4145-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4145-112">Return value</span></span>

<span data-ttu-id="e4145-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e4145-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e4145-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4145-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e4145-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e4145-115">Return code</span></span>                                                                                                            | <span data-ttu-id="e4145-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4145-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4145-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4145-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e4145-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e4145-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4145-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e4145-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e4145-120">A propriedade especificada pela *chave* não é um tipo de **LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="e4145-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="e4145-121"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="e4145-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e4145-122">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="e4145-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="e4145-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4145-123">Examples</span></span>

<span data-ttu-id="e4145-124">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="e4145-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4145-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4145-125">Requirements</span></span>



| <span data-ttu-id="e4145-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4145-126">Requirement</span></span> | <span data-ttu-id="e4145-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e4145-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4145-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4145-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e4145-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4145-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4145-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4145-130">Library</span></span><br/> | <dl> <span data-ttu-id="e4145-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4145-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4145-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4145-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4145-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e4145-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e4145-134">**IPortableDeviceValues::GetAt**</span><span class="sxs-lookup"><span data-stu-id="e4145-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="e4145-135">**IPortableDeviceValues:: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e4145-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="e4145-136">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="e4145-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="e4145-137">Recuperando formatos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="e4145-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="e4145-138">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="e4145-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




