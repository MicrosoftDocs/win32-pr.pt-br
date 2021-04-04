---
title: Método IMediaRendererActionInformation IsMuteAvailable
description: Recupera um valor que indica se o DMR é capaz de desativar o áudio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API de streaming de mídia do método IsMuteAvailable
- API de streaming de mídia do método IsMuteAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007435"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="a74c6-106">Método IMediaRendererActionInformation:: IsMuteAvailable</span><span class="sxs-lookup"><span data-stu-id="a74c6-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="a74c6-107">Recupera um valor que indica se o DMR é capaz de desativar o áudio.</span><span class="sxs-lookup"><span data-stu-id="a74c6-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a74c6-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="a74c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a74c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74c6-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a74c6-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a74c6-111">Um valor booliano que será **true** se o DMR for capaz de desativar o áudio e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="a74c6-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74c6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a74c6-112">Return value</span></span>

<span data-ttu-id="a74c6-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a74c6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a74c6-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a74c6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a74c6-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a74c6-115">Return code</span></span>                                                                          | <span data-ttu-id="a74c6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a74c6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a74c6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a74c6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a74c6-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a74c6-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a74c6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a74c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74c6-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="a74c6-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

