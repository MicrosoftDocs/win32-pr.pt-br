---
description: O método GetUnsignedIntegerValue recupera um valor ULONG (tipo VT \_ UI4) especificado por uma chave.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Método IPortableDeviceValues:: GetUnsignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747689"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="8e80b-103">Método IPortableDeviceValues:: GetUnsignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="8e80b-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="8e80b-104">O método **GetUnsignedIntegerValue** recupera um valor **ULONG** (tipo VT \_ UI4) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="8e80b-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e80b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e80b-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8e80b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e80b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e80b-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e80b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e80b-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8e80b-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8e80b-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8e80b-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e80b-110">Ponteiro para o valor **ULONG** recuperado.</span><span class="sxs-lookup"><span data-stu-id="8e80b-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e80b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e80b-111">Return value</span></span>

<span data-ttu-id="8e80b-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8e80b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8e80b-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e80b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8e80b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8e80b-114">Return code</span></span>                                                                                                            | <span data-ttu-id="8e80b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e80b-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e80b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e80b-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="8e80b-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8e80b-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8e80b-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="8e80b-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="8e80b-119">A propriedade especificada pela *chave* não é um tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="8e80b-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="8e80b-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e80b-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="8e80b-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="8e80b-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="8e80b-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e80b-122">Examples</span></span>

<span data-ttu-id="8e80b-123">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="8e80b-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e80b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e80b-124">Requirements</span></span>



| <span data-ttu-id="8e80b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e80b-125">Requirement</span></span> | <span data-ttu-id="8e80b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8e80b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e80b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e80b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8e80b-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e80b-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e80b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e80b-129">Library</span></span><br/> | <dl> <span data-ttu-id="8e80b-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e80b-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e80b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e80b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e80b-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8e80b-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8e80b-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="8e80b-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="8e80b-134">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="8e80b-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="8e80b-135">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="8e80b-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="8e80b-136">Recuperando os recursos de renderização suportados por um dispositivo</span><span class="sxs-lookup"><span data-stu-id="8e80b-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




