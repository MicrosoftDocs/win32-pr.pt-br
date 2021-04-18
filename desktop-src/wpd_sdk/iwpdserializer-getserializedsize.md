---
description: O método GetSerializedSize calcula o tamanho do buffer necessário para manter uma interface IPortableDeviceValues serializada.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Método IWpdSerializer:: GetSerializedSize (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756518"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="27926-103">Método IWpdSerializer:: GetSerializedSize</span><span class="sxs-lookup"><span data-stu-id="27926-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="27926-104">O método **GetSerializedSize** calcula o tamanho do buffer necessário para manter uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) serializada.</span><span class="sxs-lookup"><span data-stu-id="27926-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="27926-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27926-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="27926-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27926-107">*pSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27926-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27926-108">Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) cujo tamanho você deseja solicitar.</span><span class="sxs-lookup"><span data-stu-id="27926-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="27926-109">*pdwSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27926-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27926-110">Ponteiro para um **DWORD** que indica o tamanho do buffer necessário para serializar *pSource*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="27926-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27926-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27926-111">Return value</span></span>

<span data-ttu-id="27926-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="27926-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="27926-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="27926-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="27926-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="27926-114">Return code</span></span>                                                                                   | <span data-ttu-id="27926-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="27926-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27926-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27926-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="27926-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="27926-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="27926-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="27926-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="27926-119">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="27926-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="27926-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="27926-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="27926-121">Não havia memória suficiente disponível para criar o buffer.</span><span class="sxs-lookup"><span data-stu-id="27926-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27926-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27926-122">Requirements</span></span>



| <span data-ttu-id="27926-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="27926-123">Requirement</span></span> | <span data-ttu-id="27926-124">Valor</span><span class="sxs-lookup"><span data-stu-id="27926-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27926-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27926-125">Header</span></span><br/>  | <dl> <span data-ttu-id="27926-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="27926-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="27926-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27926-127">Library</span></span><br/> | <dl> <span data-ttu-id="27926-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27926-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27926-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="27926-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27926-130">**Interface IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="27926-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




