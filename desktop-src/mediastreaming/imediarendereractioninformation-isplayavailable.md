---
title: Método IMediaRendererActionInformation IsPlayAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o que aceita os métodos PlayAsync e PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API de streaming de mídia do método IsPlayAvailable
- API de streaming de mídia do método IsPlayAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365955"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="0ca2f-106">Método IMediaRendererActionInformation:: IsPlayAvailable</span><span class="sxs-lookup"><span data-stu-id="0ca2f-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="0ca2f-107">Recupera um valor que indica se o DMR está atualmente aceitando o que aceita os métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .</span><span class="sxs-lookup"><span data-stu-id="0ca2f-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca2f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ca2f-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="0ca2f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ca2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca2f-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0ca2f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca2f-111">Um valor booliano que é **verdadeiro** se o DMR estiver atualmente aceitando o que aceita os métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca2f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ca2f-112">Return value</span></span>

<span data-ttu-id="0ca2f-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0ca2f-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0ca2f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0ca2f-115">Return code</span></span>                                                                          | <span data-ttu-id="0ca2f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ca2f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0ca2f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ca2f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0ca2f-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0ca2f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0ca2f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ca2f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca2f-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="0ca2f-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

