---
description: O método WriteIPortableDeviceValuesToBuffer serializa uma interface IPortableDeviceValues para uma matriz de bytes alocada pelo chamador.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Método IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766545"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="c2341-103">Método IWpdSerializer:: WriteIPortableDeviceValuesToBuffer</span><span class="sxs-lookup"><span data-stu-id="c2341-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="c2341-104">O método **WriteIPortableDeviceValuesToBuffer** serializa uma interface **IPortableDeviceValues** para uma matriz de bytes alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="c2341-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2341-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2341-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="c2341-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2341-107">*dwOutputBufferLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2341-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2341-108">**DWORD** que especifica o tamanho de *pBuffer*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c2341-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2341-109">*pResults* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2341-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2341-110">Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) para serializar.</span><span class="sxs-lookup"><span data-stu-id="c2341-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="c2341-111">*pBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2341-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2341-112">Ponteiro para um buffer alocado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="c2341-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="c2341-113">Para saber o tamanho do buffer necessário, chame **GetSerializedSize**.</span><span class="sxs-lookup"><span data-stu-id="c2341-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="c2341-114">*pdwBytesWritten* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2341-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2341-115">Ponteiro para um **DWORD** que indica o número de bytes que foi realmente gravado no buffer alocado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="c2341-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2341-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2341-116">Return value</span></span>

<span data-ttu-id="c2341-117">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c2341-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2341-118">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2341-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2341-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c2341-119">Return code</span></span>                                                                                   | <span data-ttu-id="c2341-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2341-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="c2341-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2341-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c2341-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c2341-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="c2341-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c2341-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c2341-124">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c2341-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="c2341-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c2341-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c2341-126">O buffer fornecido pelo chamador não era grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="c2341-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2341-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2341-127">Remarks</span></span>

<span data-ttu-id="c2341-128">Esse método copia uma interface **IPortableDeviceValues** em um buffer existente.</span><span class="sxs-lookup"><span data-stu-id="c2341-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="c2341-129">Se você quiser alocar um novo buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="c2341-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2341-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2341-130">Requirements</span></span>



| <span data-ttu-id="c2341-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2341-131">Requirement</span></span> | <span data-ttu-id="c2341-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c2341-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2341-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2341-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c2341-134"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2341-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2341-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2341-135">Library</span></span><br/> | <dl> <span data-ttu-id="c2341-136"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2341-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2341-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2341-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2341-138">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="c2341-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




