---
title: Método IMediaRendererActionInformation IsVolumeAvailable
description: Recupera um valor que indica se o DMR é capaz de ajustar o nível de volume de áudio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API de streaming de mídia do método IsVolumeAvailable
- API de streaming de mídia do método IsVolumeAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084478"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="b1320-106">Método IMediaRendererActionInformation:: IsVolumeAvailable</span><span class="sxs-lookup"><span data-stu-id="b1320-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="b1320-107">Recupera um valor que indica se o DMR é capaz de ajustar o nível de volume de áudio.</span><span class="sxs-lookup"><span data-stu-id="b1320-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1320-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1320-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="b1320-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1320-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1320-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b1320-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1320-111">Um valor booliano que será **true** se o DMR for capaz de ajustar o nível de volume de áudio e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="b1320-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1320-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1320-112">Return value</span></span>

<span data-ttu-id="b1320-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b1320-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b1320-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1320-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b1320-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1320-115">Return code</span></span>                                                                          | <span data-ttu-id="b1320-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1320-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b1320-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1320-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b1320-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b1320-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b1320-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1320-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1320-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="b1320-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

