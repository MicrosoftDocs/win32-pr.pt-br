---
title: Método IMediaRenderer PauseAsync
description: Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual. | Método IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API de streaming de mídia do método PauseAsync
- API de streaming de mídia do método PauseAsync, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105812040"
---
# <a name="imediarendererpauseasync-method"></a><span data-ttu-id="47efb-107">IMediaRenderer: método auseAsync de:P</span><span class="sxs-lookup"><span data-stu-id="47efb-107">IMediaRenderer::PauseAsync method</span></span>

<span data-ttu-id="47efb-108">Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual.</span><span class="sxs-lookup"><span data-stu-id="47efb-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="47efb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47efb-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="47efb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47efb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47efb-111">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="47efb-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47efb-112">Recebe uma referência a um objeto [**PlaybackOperation**](playbackoperation.md) que é usado para obter resultados da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="47efb-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47efb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47efb-113">Return value</span></span>

<span data-ttu-id="47efb-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="47efb-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="47efb-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="47efb-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="47efb-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="47efb-116">Return code</span></span>                                                                          | <span data-ttu-id="47efb-117">Description</span><span class="sxs-lookup"><span data-stu-id="47efb-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="47efb-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47efb-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="47efb-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="47efb-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="47efb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="47efb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47efb-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="47efb-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





