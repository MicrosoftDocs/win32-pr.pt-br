---
description: O método GetSignedIntegerValue recupera um valor longo (tipo VT \_ i4) especificado por uma chave.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'Método IPortableDeviceValues:: GetSignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752780"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="53882-103">Método IPortableDeviceValues:: GetSignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="53882-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="53882-104">O método **GetSignedIntegerValue** recupera um valor **longo** (tipo VT \_ i4) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="53882-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="53882-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53882-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="53882-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53882-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53882-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53882-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="53882-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="53882-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53882-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53882-110">Ponteiro para o valor **longo** recuperado.</span><span class="sxs-lookup"><span data-stu-id="53882-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53882-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53882-111">Return value</span></span>

<span data-ttu-id="53882-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53882-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53882-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="53882-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53882-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="53882-114">Return code</span></span>                                                                                                            | <span data-ttu-id="53882-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="53882-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="53882-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53882-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="53882-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="53882-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="53882-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="53882-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="53882-119">A propriedade especificada pela *chave* não é um tipo **longo** .</span><span class="sxs-lookup"><span data-stu-id="53882-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="53882-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="53882-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="53882-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="53882-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53882-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53882-122">Requirements</span></span>



| <span data-ttu-id="53882-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="53882-123">Requirement</span></span> | <span data-ttu-id="53882-124">Valor</span><span class="sxs-lookup"><span data-stu-id="53882-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53882-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53882-125">Header</span></span><br/>  | <dl> <span data-ttu-id="53882-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="53882-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="53882-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53882-127">Library</span></span><br/> | <dl> <span data-ttu-id="53882-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53882-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53882-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="53882-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53882-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="53882-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="53882-131">**IPortableDeviceValues::SetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="53882-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




