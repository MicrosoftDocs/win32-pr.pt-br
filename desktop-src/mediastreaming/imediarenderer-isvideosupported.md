---
title: Método IMediaRenderer IsVideoSupported
description: Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API de streaming de mídia do método IsVideoSupported
- API de streaming de mídia do método IsVideoSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293346"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="c5c68-106">Método IMediaRenderer:: IsVideoSupported</span><span class="sxs-lookup"><span data-stu-id="c5c68-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="c5c68-107">Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5c68-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c68-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5c68-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="c5c68-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5c68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c68-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c5c68-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c68-111">Um valor booliano que será **true** se o DMR for capaz de reproduzir conteúdo de vídeo e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="c5c68-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c68-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5c68-112">Return value</span></span>

<span data-ttu-id="c5c68-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c5c68-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c5c68-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c5c68-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c5c68-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c5c68-115">Return code</span></span>                                                                          | <span data-ttu-id="c5c68-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5c68-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c5c68-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5c68-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c5c68-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c5c68-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c5c68-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5c68-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c68-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="c5c68-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





