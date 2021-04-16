---
description: O método GetKeyValue recupera um valor de PROPERTYKEY especificado por uma chave.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'Método IPortableDeviceValues:: GetKeyValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751361"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="0c441-103">Método IPortableDeviceValues:: GetKeyValue</span><span class="sxs-lookup"><span data-stu-id="0c441-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="0c441-104">O método **GetKeyValue** recupera um valor de **PROPERTYKEY** especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="0c441-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c441-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c441-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0c441-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c441-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c441-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c441-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="0c441-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0c441-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c441-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c441-110">Ponteiro para o valor de **PROPERTYKEY** recuperado.</span><span class="sxs-lookup"><span data-stu-id="0c441-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c441-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c441-111">Return value</span></span>

<span data-ttu-id="0c441-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c441-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c441-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c441-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c441-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c441-114">Return code</span></span>                                                                                                            | <span data-ttu-id="0c441-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c441-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c441-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c441-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="0c441-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0c441-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0c441-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="0c441-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="0c441-119">A propriedade especificada pela *chave* não é um tipo **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="0c441-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="0c441-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c441-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="0c441-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="0c441-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="0c441-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c441-122">Requirements</span></span>



| <span data-ttu-id="0c441-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c441-123">Requirement</span></span> | <span data-ttu-id="0c441-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0c441-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c441-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c441-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0c441-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c441-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c441-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c441-127">Library</span></span><br/> | <dl> <span data-ttu-id="0c441-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c441-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c441-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c441-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c441-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0c441-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0c441-131">**IPortableDeviceValues::SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="0c441-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




