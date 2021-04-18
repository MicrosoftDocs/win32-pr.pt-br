---
title: Método IMediaRenderer IsAudioSupported
description: Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API de streaming de mídia do método IsAudioSupported
- API de streaming de mídia do método IsAudioSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105814571"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="8a235-106">Método IMediaRenderer:: IsAudioSupported</span><span class="sxs-lookup"><span data-stu-id="8a235-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="8a235-107">Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="8a235-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a235-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a235-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="8a235-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a235-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a235-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8a235-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a235-111">Um valor booliano que será **true** se o DMR for capaz de reproduzir o conteúdo de áudio e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="8a235-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a235-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a235-112">Return value</span></span>

<span data-ttu-id="8a235-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a235-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a235-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a235-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a235-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a235-115">Return code</span></span>                                                                          | <span data-ttu-id="8a235-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a235-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a235-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a235-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a235-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8a235-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8a235-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a235-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a235-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="8a235-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





