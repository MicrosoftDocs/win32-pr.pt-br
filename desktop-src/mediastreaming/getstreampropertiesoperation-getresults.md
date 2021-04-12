---
title: Método GetStreamPropertiesOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetStreamPropertiesOperation
- API de streaming de mídia da interface GetStreamPropertiesOperation, método GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365932"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="9d3a8-106">Método GetStreamPropertiesOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="9d3a8-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="9d3a8-107">Retorna os resultados da operação assíncrona iniciada pelo [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d3a8-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d3a8-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="9d3a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d3a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3a8-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9d3a8-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="9d3a8-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9d3a8-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9d3a8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d3a8-112">Return value</span></span>

<span data-ttu-id="9d3a8-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9d3a8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9d3a8-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d3a8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9d3a8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9d3a8-115">Return code</span></span>                                                                          | <span data-ttu-id="9d3a8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d3a8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9d3a8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d3a8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9d3a8-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9d3a8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9d3a8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d3a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3a8-120">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="9d3a8-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

