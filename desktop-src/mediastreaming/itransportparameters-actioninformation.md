---
title: Método ITransportParameters ActionInformation
description: Obtém uma interface IMediaRendererActionInformation que fornece informações sobre quais métodos podem ser invocados no momento no DMR.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API de streaming de mídia do método ActionInformation
- API de streaming de mídia do método ActionInformation, interface ITransportParameters
- API de streaming de mídia da interface ITransportParameters, método ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007448"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="888b0-106">Método ITransportParameters:: ActionInformation</span><span class="sxs-lookup"><span data-stu-id="888b0-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="888b0-107">Obtém uma interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) que fornece informações sobre quais métodos podem ser invocados no momento no DMR.</span><span class="sxs-lookup"><span data-stu-id="888b0-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="888b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="888b0-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="888b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="888b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888b0-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="888b0-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="888b0-111">Recebe uma referência a uma interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="888b0-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888b0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="888b0-112">Return value</span></span>

<span data-ttu-id="888b0-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="888b0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="888b0-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="888b0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="888b0-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="888b0-115">Return code</span></span>                                                                          | <span data-ttu-id="888b0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="888b0-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="888b0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="888b0-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="888b0-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="888b0-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="888b0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="888b0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888b0-120">**ITransportParameters**</span><span class="sxs-lookup"><span data-stu-id="888b0-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

