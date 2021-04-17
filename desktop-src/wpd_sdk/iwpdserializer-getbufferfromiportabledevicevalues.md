---
description: O método GetBufferFromIPortableDeviceValues serializa uma interface IPortableDeviceValues enviada para uma matriz de bytes alocada. A matriz de bytes retornada é alocada para o chamador e deve ser liberada pelo chamador usando CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Método IWpdSerializer:: GetBufferFromIPortableDeviceValues (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798267"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="345ab-104">Método IWpdSerializer:: GetBufferFromIPortableDeviceValues</span><span class="sxs-lookup"><span data-stu-id="345ab-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="345ab-105">O método **GetBufferFromIPortableDeviceValues** serializa uma interface **IPortableDeviceValues** enviada para uma matriz de bytes alocada.</span><span class="sxs-lookup"><span data-stu-id="345ab-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="345ab-106">A matriz de bytes retornada é alocada para o chamador e deve ser liberada pelo chamador usando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="345ab-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="345ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="345ab-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="345ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="345ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345ab-109">*pSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="345ab-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="345ab-110">Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) para serializar.</span><span class="sxs-lookup"><span data-stu-id="345ab-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="345ab-111">*ppBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="345ab-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="345ab-112">Ponteiro para um **byte \* *_ que contém os dados serializados. Os dispositivos portáteis do Windows alocam essa memória; o chamador deve liberá-lo chamando _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="345ab-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="345ab-113">*pdwBufferSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="345ab-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="345ab-114">Ponteiro para um **DWORD** que especifica o tamanho do buffer alocado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="345ab-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="345ab-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="345ab-115">Return value</span></span>

<span data-ttu-id="345ab-116">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="345ab-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="345ab-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="345ab-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="345ab-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="345ab-118">Return code</span></span>                                                                                   | <span data-ttu-id="345ab-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="345ab-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="345ab-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="345ab-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="345ab-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="345ab-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="345ab-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="345ab-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="345ab-123">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="345ab-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="345ab-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="345ab-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="345ab-125">Não havia memória suficiente disponível para criar o buffer.</span><span class="sxs-lookup"><span data-stu-id="345ab-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="345ab-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345ab-126">Requirements</span></span>



| <span data-ttu-id="345ab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="345ab-127">Requirement</span></span> | <span data-ttu-id="345ab-128">Valor</span><span class="sxs-lookup"><span data-stu-id="345ab-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345ab-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="345ab-129">Header</span></span><br/>  | <dl> <span data-ttu-id="345ab-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="345ab-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="345ab-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="345ab-131">Library</span></span><br/> | <dl> <span data-ttu-id="345ab-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="345ab-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345ab-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="345ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345ab-134">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="345ab-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




