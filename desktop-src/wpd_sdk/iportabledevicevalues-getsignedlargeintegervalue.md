---
description: O método GetSignedLargeIntegerValue recupera um valor de LONGLONG (tipo VT \_ i8) especificado por uma chave.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'Método IPortableDeviceValues:: GetSignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758656"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="8b793-103">Método IPortableDeviceValues:: GetSignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="8b793-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="8b793-104">O método **GetSignedLargeIntegerValue** recupera um valor de **LONGLONG** (tipo VT \_ i8) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="8b793-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b793-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b793-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8b793-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b793-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b793-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b793-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8b793-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8b793-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8b793-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b793-110">Ponteiro para o valor **ULONG** recuperado.</span><span class="sxs-lookup"><span data-stu-id="8b793-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b793-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b793-111">Return value</span></span>

<span data-ttu-id="8b793-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8b793-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8b793-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b793-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8b793-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8b793-114">Return code</span></span>                                                                                                            | <span data-ttu-id="8b793-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b793-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b793-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b793-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="8b793-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8b793-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="8b793-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="8b793-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="8b793-119">A propriedade especificada por *chave* não é um tipo **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="8b793-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="8b793-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="8b793-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="8b793-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="8b793-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="8b793-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b793-122">Requirements</span></span>



| <span data-ttu-id="8b793-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b793-123">Requirement</span></span> | <span data-ttu-id="8b793-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8b793-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b793-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b793-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8b793-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b793-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b793-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b793-127">Library</span></span><br/> | <dl> <span data-ttu-id="8b793-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b793-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b793-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b793-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b793-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8b793-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8b793-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="8b793-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




