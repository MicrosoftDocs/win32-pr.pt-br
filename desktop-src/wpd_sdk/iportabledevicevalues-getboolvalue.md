---
description: O método getboolvalue recupera um valor booliano (tipo VT \_ bool) especificado por uma chave.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Método IPortableDeviceValues:: getboolvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750558"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="f877f-103">Método IPortableDeviceValues:: getboolvalue</span><span class="sxs-lookup"><span data-stu-id="f877f-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="f877f-104">O método **Getboolvalue** recupera um valor **booliano** (tipo VT \_ bool) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="f877f-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f877f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f877f-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f877f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f877f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f877f-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f877f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f877f-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="f877f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f877f-109">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f877f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f877f-110">Ponteiro para o valor **bool** recuperado.</span><span class="sxs-lookup"><span data-stu-id="f877f-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f877f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f877f-111">Return value</span></span>

<span data-ttu-id="f877f-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f877f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f877f-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f877f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f877f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f877f-114">Return code</span></span>                                                                                                            | <span data-ttu-id="f877f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f877f-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="f877f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f877f-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="f877f-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f877f-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f877f-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="f877f-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="f877f-119">A propriedade especificada pela *chave* não é um tipo **bool** .</span><span class="sxs-lookup"><span data-stu-id="f877f-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="f877f-120"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="f877f-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="f877f-121">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="f877f-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f877f-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f877f-122">Examples</span></span>

<span data-ttu-id="f877f-123">Para obter um exemplo de como usar esse método, consulte [definindo propriedades para um único objeto](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="f877f-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f877f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f877f-124">Requirements</span></span>



| <span data-ttu-id="f877f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f877f-125">Requirement</span></span> | <span data-ttu-id="f877f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f877f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f877f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f877f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f877f-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f877f-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f877f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f877f-129">Library</span></span><br/> | <dl> <span data-ttu-id="f877f-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f877f-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f877f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f877f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f877f-132">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f877f-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f877f-133">**IPortableDeviceValues:: SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="f877f-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="f877f-134">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="f877f-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="f877f-135">Definindo propriedades para um único objeto</span><span class="sxs-lookup"><span data-stu-id="f877f-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="f877f-136">Gravando Propriedades de objeto de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f877f-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




