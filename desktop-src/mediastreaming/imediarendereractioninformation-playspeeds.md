---
title: Método IMediaRendererActionInformation PlaySpeeds
description: Recupera a lista completa de valores PlaySpeed que são aceitos pelo DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API de streaming de mídia do método PlaySpeeds
- API de streaming de mídia do método PlaySpeeds, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294010"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="e046d-106">IMediaRendererActionInformation: método laySpeeds de:P</span><span class="sxs-lookup"><span data-stu-id="e046d-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="e046d-107">Recupera a lista completa de valores [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que são aceitos pelo DMR.</span><span class="sxs-lookup"><span data-stu-id="e046d-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="e046d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e046d-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="e046d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e046d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e046d-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e046d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e046d-111">Recebe um vetor de estruturas [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) especificando a lista completa de valores de **PlaySpeed** que são aceitos pelo DMR.</span><span class="sxs-lookup"><span data-stu-id="e046d-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e046d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e046d-112">Return value</span></span>

<span data-ttu-id="e046d-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e046d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e046d-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e046d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e046d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e046d-115">Return code</span></span>                                                                          | <span data-ttu-id="e046d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e046d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e046d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e046d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e046d-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e046d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e046d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e046d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e046d-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="e046d-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

