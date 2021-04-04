---
title: Método IMediaRenderer StopAsync
description: Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual. | Método IMediaRenderer StopAsync
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- API de streaming de mídia do método StopAsync
- API de streaming de mídia do método StopAsync, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837885"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="b1880-107">Método IMediaRenderer:: StopAsync</span><span class="sxs-lookup"><span data-stu-id="b1880-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="b1880-108">Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual.</span><span class="sxs-lookup"><span data-stu-id="b1880-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1880-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1880-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="b1880-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1880-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1880-111">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b1880-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1880-112">Recebe uma referência a um objeto [**PlaybackOperation**](playbackoperation.md) que é usado para obter resultados da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b1880-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1880-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1880-113">Return value</span></span>

<span data-ttu-id="b1880-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b1880-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b1880-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1880-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b1880-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1880-116">Return code</span></span>                                                                          | <span data-ttu-id="b1880-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1880-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b1880-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1880-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b1880-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b1880-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b1880-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1880-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1880-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="b1880-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





