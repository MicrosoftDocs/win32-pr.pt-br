---
title: Método IMediaRendererActionInformation IsSeekAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API de streaming de mídia do método IsSeekAvailable
- API de streaming de mídia do método IsSeekAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823739"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="d73ed-106">Método IMediaRendererActionInformation:: IsSeekAvailable</span><span class="sxs-lookup"><span data-stu-id="d73ed-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="d73ed-107">Recupera um valor que indica se o DMR está atualmente aceitando o método [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .</span><span class="sxs-lookup"><span data-stu-id="d73ed-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73ed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d73ed-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d73ed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d73ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73ed-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d73ed-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d73ed-111">Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="d73ed-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73ed-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d73ed-112">Return value</span></span>

<span data-ttu-id="d73ed-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d73ed-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d73ed-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d73ed-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d73ed-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d73ed-115">Return code</span></span>                                                                          | <span data-ttu-id="d73ed-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d73ed-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d73ed-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d73ed-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d73ed-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d73ed-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d73ed-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d73ed-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73ed-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="d73ed-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

