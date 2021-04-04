---
title: Método IMediaRendererActionInformation IsPauseAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API de streaming de mídia do método IsPauseAvailable
- API de streaming de mídia do método IsPauseAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823740"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="17605-106">Método IMediaRendererActionInformation:: IsPauseAvailable</span><span class="sxs-lookup"><span data-stu-id="17605-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="17605-107">Recupera um valor que indica se o DMR está atualmente aceitando o método [**PauseAsync**](imediarenderer-pauseasync.md) .</span><span class="sxs-lookup"><span data-stu-id="17605-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17605-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17605-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="17605-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17605-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17605-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="17605-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17605-111">Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**PauseAsync**](imediarenderer-pauseasync.md) e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="17605-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17605-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17605-112">Return value</span></span>

<span data-ttu-id="17605-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="17605-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17605-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="17605-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="17605-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="17605-115">Return code</span></span>                                                                          | <span data-ttu-id="17605-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="17605-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="17605-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17605-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="17605-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="17605-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="17605-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="17605-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17605-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="17605-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

