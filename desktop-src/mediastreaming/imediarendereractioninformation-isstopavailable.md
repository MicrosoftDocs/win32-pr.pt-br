---
title: Método IMediaRendererActionInformation IsStopAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API de streaming de mídia do método IsStopAvailable
- API de streaming de mídia do método IsStopAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084514"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="0c771-106">Método IMediaRendererActionInformation:: IsStopAvailable</span><span class="sxs-lookup"><span data-stu-id="0c771-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="0c771-107">Recupera um valor que indica se o DMR está atualmente aceitando o método [**StopAsync**](imediarenderer-stopasync.md) .</span><span class="sxs-lookup"><span data-stu-id="0c771-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c771-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c771-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="0c771-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c771-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c771-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0c771-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c771-111">Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**StopAsync**](imediarenderer-stopasync.md) e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="0c771-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c771-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c771-112">Return value</span></span>

<span data-ttu-id="0c771-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c771-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c771-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c771-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c771-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c771-115">Return code</span></span>                                                                          | <span data-ttu-id="0c771-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c771-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0c771-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c771-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0c771-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0c771-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0c771-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c771-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c771-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="0c771-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

