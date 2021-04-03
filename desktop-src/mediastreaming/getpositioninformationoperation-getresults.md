---
title: Método GetPositionInformationOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetPositionInformationOperation
- API de streaming de mídia da interface GetPositionInformationOperation, método GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640964"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="7c242-106">Método GetPositionInformationOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="7c242-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="7c242-107">Retorna os resultados da operação assíncrona iniciada pelo [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="7c242-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c242-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c242-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="7c242-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c242-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c242-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7c242-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7c242-111">Uma referência a uma estrutura [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) que contém os resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="7c242-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c242-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c242-112">Return value</span></span>

<span data-ttu-id="7c242-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7c242-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7c242-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7c242-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7c242-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7c242-115">Return code</span></span>                                                                          | <span data-ttu-id="7c242-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c242-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7c242-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c242-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7c242-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7c242-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c242-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c242-119">Remarks</span></span>

<span data-ttu-id="7c242-120">O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](getpositioninformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="7c242-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c242-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c242-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c242-122">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="7c242-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

