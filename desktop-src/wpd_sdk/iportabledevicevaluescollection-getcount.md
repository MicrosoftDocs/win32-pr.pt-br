---
description: 'Método IPortableDeviceValuesCollection:: GetCount – o método GetCount recupera o número de itens na coleção.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Método IPortableDeviceValuesCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083174"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="9cef0-103">Método IPortableDeviceValuesCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="9cef0-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="9cef0-104">O método **GetCount** recupera o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="9cef0-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cef0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cef0-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="9cef0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cef0-107">*pcElems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cef0-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cef0-108">Ponteiro para um **DWORD** que contém o número de interfaces **IPortableDeviceValues** na coleção.</span><span class="sxs-lookup"><span data-stu-id="9cef0-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cef0-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9cef0-109">Return value</span></span>

<span data-ttu-id="9cef0-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9cef0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9cef0-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cef0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9cef0-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9cef0-112">Return code</span></span>                                                                               | <span data-ttu-id="9cef0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cef0-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="9cef0-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9cef0-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9cef0-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9cef0-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="9cef0-116"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9cef0-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="9cef0-117">Um argumento de ponteiro necessário era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9cef0-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9cef0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cef0-118">Requirements</span></span>



| <span data-ttu-id="9cef0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cef0-119">Requirement</span></span> | <span data-ttu-id="9cef0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9cef0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cef0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cef0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9cef0-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cef0-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cef0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cef0-123">Library</span></span><br/> | <dl> <span data-ttu-id="9cef0-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cef0-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cef0-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9cef0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cef0-126">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="9cef0-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




