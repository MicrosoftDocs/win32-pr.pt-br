---
description: O método GetCount recupera o número de chaves nesta coleção.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'Método IPortableDeviceKeyCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773061"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="fc796-103">Método IPortableDeviceKeyCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="fc796-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="fc796-104">O método **GetCount** recupera o número de chaves nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="fc796-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc796-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc796-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="fc796-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc796-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc796-107">*pcElems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc796-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc796-108">Ponteiro para um **DWORD** que contém o número de chaves na coleção.</span><span class="sxs-lookup"><span data-stu-id="fc796-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc796-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc796-109">Return value</span></span>

<span data-ttu-id="fc796-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fc796-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fc796-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc796-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fc796-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fc796-112">Return code</span></span>                                                                               | <span data-ttu-id="fc796-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc796-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="fc796-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc796-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fc796-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fc796-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="fc796-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc796-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fc796-117">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="fc796-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="fc796-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc796-118">Examples</span></span>

<span data-ttu-id="fc796-119">Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="fc796-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc796-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc796-120">Requirements</span></span>



| <span data-ttu-id="fc796-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc796-121">Requirement</span></span> | <span data-ttu-id="fc796-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fc796-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc796-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc796-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fc796-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc796-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc796-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc796-125">Library</span></span><br/> | <dl> <span data-ttu-id="fc796-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc796-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc796-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc796-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc796-128">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="fc796-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="fc796-129">Recuperando eventos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="fc796-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="fc796-130">Recuperando métodos de serviço com suporte</span><span class="sxs-lookup"><span data-stu-id="fc796-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




