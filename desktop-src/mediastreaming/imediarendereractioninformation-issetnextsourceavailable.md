---
title: Método IMediaRendererActionInformation IsSetNextSourceAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método SetNextSourceFromUriAsync, o método SetNextSourceFromStreamAsync ou o método SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API de streaming de mídia do método IsSetNextSourceAvailable
- API de streaming de mídia do método IsSetNextSourceAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsSetNextSourceAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640747"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="46dcb-106">Método IMediaRendererActionInformation:: IsSetNextSourceAvailable</span><span class="sxs-lookup"><span data-stu-id="46dcb-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="46dcb-107">Recupera um valor que indica se o DMR está atualmente aceitando o método [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , o método [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou o método [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .</span><span class="sxs-lookup"><span data-stu-id="46dcb-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dcb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46dcb-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="46dcb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46dcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46dcb-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="46dcb-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46dcb-111">Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , o método [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou o método [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="46dcb-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46dcb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46dcb-112">Return value</span></span>

<span data-ttu-id="46dcb-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46dcb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="46dcb-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46dcb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="46dcb-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="46dcb-115">Return code</span></span>                                                                          | <span data-ttu-id="46dcb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="46dcb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="46dcb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46dcb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46dcb-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="46dcb-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="46dcb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="46dcb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46dcb-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="46dcb-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

