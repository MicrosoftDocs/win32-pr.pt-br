---
description: O método getguidvalue recupera um valor de GUID (tipo VT \_ CLSID) especificado por uma chave.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'Método IPortableDeviceValues:: getguidvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752138"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="d044b-103">Método IPortableDeviceValues:: getguidvalue</span><span class="sxs-lookup"><span data-stu-id="d044b-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="d044b-104">O método **Getguidvalue** recupera um valor de **GUID** (tipo VT \_ CLSID) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="d044b-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d044b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d044b-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d044b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d044b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d044b-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d044b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d044b-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="d044b-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d044b-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d044b-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d044b-110">Ponteiro para o valor **GUID** recuperado.</span><span class="sxs-lookup"><span data-stu-id="d044b-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d044b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d044b-111">Return value</span></span>

<span data-ttu-id="d044b-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d044b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d044b-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d044b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d044b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d044b-114">Return code</span></span>                                                                                                            | <span data-ttu-id="d044b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d044b-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d044b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d044b-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d044b-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d044b-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d044b-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="d044b-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="d044b-119">A propriedade especificada pela *chave* não é um tipo de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="d044b-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="d044b-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="d044b-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d044b-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="d044b-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d044b-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d044b-122">Examples</span></span>

<span data-ttu-id="d044b-123">Para obter um exemplo de como usar esse método, consulte [recuperando métodos de serviço com suporte](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d044b-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d044b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d044b-124">Requirements</span></span>



| <span data-ttu-id="d044b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d044b-125">Requirement</span></span> | <span data-ttu-id="d044b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d044b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d044b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d044b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d044b-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d044b-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d044b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d044b-129">Library</span></span><br/> | <dl> <span data-ttu-id="d044b-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d044b-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d044b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d044b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d044b-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d044b-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d044b-133">**IPortableDeviceValues:: setguidvalue**</span><span class="sxs-lookup"><span data-stu-id="d044b-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="d044b-134">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="d044b-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="d044b-135">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="d044b-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




