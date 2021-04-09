---
title: Método IMediaRenderer ActionInformation
description: Recupera informações sobre quais métodos podem ser invocados atualmente no DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API de streaming de mídia do método ActionInformation
- API de streaming de mídia do método ActionInformation, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007463"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="45106-106">Método IMediaRenderer:: ActionInformation</span><span class="sxs-lookup"><span data-stu-id="45106-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="45106-107">Recupera informações sobre quais métodos podem ser invocados atualmente no DMR.</span><span class="sxs-lookup"><span data-stu-id="45106-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="45106-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45106-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="45106-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45106-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45106-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="45106-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45106-111">Recebe uma referência a uma interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="45106-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45106-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45106-112">Return value</span></span>

<span data-ttu-id="45106-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="45106-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="45106-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="45106-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="45106-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="45106-115">Return code</span></span>                                                                          | <span data-ttu-id="45106-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="45106-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="45106-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45106-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="45106-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="45106-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="45106-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="45106-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45106-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="45106-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

