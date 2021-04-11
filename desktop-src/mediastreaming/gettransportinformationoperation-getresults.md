---
title: Método GetResults GetTransportInformationOperation
description: Retorna os resultados da operação assíncrona iniciada pelo GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetTransportInformationOperation
- API de streaming de mídia da interface GetTransportInformationOperation, método GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365957"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="2ff62-106">Método GetTransportInformationOperation:: GetResults</span><span class="sxs-lookup"><span data-stu-id="2ff62-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="2ff62-107">Retorna os resultados da operação assíncrona iniciada pelo [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="2ff62-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff62-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ff62-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="2ff62-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ff62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff62-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2ff62-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff62-111">Uma referência a uma estrutura [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) que contém os resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="2ff62-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff62-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ff62-112">Return value</span></span>

<span data-ttu-id="2ff62-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2ff62-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2ff62-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ff62-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2ff62-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2ff62-115">Return code</span></span>                                                                          | <span data-ttu-id="2ff62-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ff62-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2ff62-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff62-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2ff62-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2ff62-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ff62-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ff62-119">Remarks</span></span>

<span data-ttu-id="2ff62-120">O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](gettransportinformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff62-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ff62-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ff62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff62-122">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="2ff62-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

