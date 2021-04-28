---
description: 'Método IPortableDeviceValues:: Clear – o método Clear exclui todos os itens da coleção.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'Método IPortableDeviceValues:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109894"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="4ceb8-103">Método IPortableDeviceValues:: Clear</span><span class="sxs-lookup"><span data-stu-id="4ceb8-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="4ceb8-104">O método **Clear** exclui todos os itens da coleção.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ceb8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ceb8-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="4ceb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ceb8-106">Parameters</span></span>

<span data-ttu-id="4ceb8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ceb8-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4ceb8-108">Return value</span></span>

<span data-ttu-id="4ceb8-109">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4ceb8-110">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4ceb8-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4ceb8-111">Return code</span></span>                                                                          | <span data-ttu-id="4ceb8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ceb8-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4ceb8-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb8-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4ceb8-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ceb8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ceb8-115">Remarks</span></span>

<span data-ttu-id="4ceb8-116">Esse método libera a memória para todos os itens alocados dinamicamente na coleção.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="4ceb8-117">Para interfaces, ele chama **Release**.</span><span class="sxs-lookup"><span data-stu-id="4ceb8-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ceb8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ceb8-118">Requirements</span></span>



| <span data-ttu-id="4ceb8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ceb8-119">Requirement</span></span> | <span data-ttu-id="4ceb8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4ceb8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ceb8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ceb8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4ceb8-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb8-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ceb8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ceb8-123">Library</span></span><br/> | <dl> <span data-ttu-id="4ceb8-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb8-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ceb8-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4ceb8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ceb8-126">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4ceb8-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




