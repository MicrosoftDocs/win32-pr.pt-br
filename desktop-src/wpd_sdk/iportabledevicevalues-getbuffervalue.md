---
description: O método getbuffervalue recupera um valor de matriz de bytes (tipo VT \_ vector \| VT \_ UI1) especificado por uma chave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Método IPortableDeviceValues:: getbuffervalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771481"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="0c738-103">Método IPortableDeviceValues:: getbuffervalue</span><span class="sxs-lookup"><span data-stu-id="0c738-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="0c738-104">O método **Getbuffervalue** recupera um valor de **matriz de bytes** (tipo VT \_ vector \| VT \_ UI1) especificado por uma chave.</span><span class="sxs-lookup"><span data-stu-id="0c738-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c738-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c738-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="0c738-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c738-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c738-107">*chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c738-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c738-108">Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="0c738-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0c738-109">*ppValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c738-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c738-110">Ponteiro para o **valor de byte \* *_ recuperado. O chamador é responsável por liberar a memória chamando _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="0c738-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="0c738-111">*pcbValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c738-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c738-112">Ponteiro para o tamanho de *ppValue*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0c738-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c738-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c738-113">Return value</span></span>

<span data-ttu-id="0c738-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c738-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c738-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c738-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c738-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c738-116">Return code</span></span>                                                                                                            | <span data-ttu-id="0c738-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c738-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c738-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c738-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="0c738-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0c738-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0c738-120"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="0c738-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="0c738-121">A propriedade especificada pela *chave* não é um tipo de **byte** \* .</span><span class="sxs-lookup"><span data-stu-id="0c738-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="0c738-122"><dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt></span><span class="sxs-lookup"><span data-stu-id="0c738-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="0c738-123">A propriedade especificada pela *chave* não está na coleção.</span><span class="sxs-lookup"><span data-stu-id="0c738-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c738-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c738-124">Remarks</span></span>

<span data-ttu-id="0c738-125">Não há suporte para a recuperação de um buffer **nulo** ou de um buffer de tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="0c738-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c738-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c738-126">Requirements</span></span>



| <span data-ttu-id="0c738-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c738-127">Requirement</span></span> | <span data-ttu-id="0c738-128">Valor</span><span class="sxs-lookup"><span data-stu-id="0c738-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c738-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c738-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0c738-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c738-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c738-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c738-131">Library</span></span><br/> | <dl> <span data-ttu-id="0c738-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c738-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c738-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c738-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c738-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0c738-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0c738-135">**IPortableDeviceValues:: setbuffervalue**</span><span class="sxs-lookup"><span data-stu-id="0c738-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




