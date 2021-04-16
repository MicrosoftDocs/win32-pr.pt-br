---
title: Método IMediaRenderer IsImageSupported
description: Recupera um valor que indica se o DMR é capaz de exibir imagens.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API de streaming de mídia do método IsImageSupported
- API de streaming de mídia do método IsImageSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105772642"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="d9887-106">Método IMediaRenderer:: IsImageSupported</span><span class="sxs-lookup"><span data-stu-id="d9887-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="d9887-107">Recupera um valor que indica se o DMR é capaz de exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="d9887-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9887-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9887-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d9887-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9887-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9887-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d9887-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9887-111">Um valor booliano que será **true** se o DMR for capaz de exibir imagens e **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="d9887-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9887-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9887-112">Return value</span></span>

<span data-ttu-id="d9887-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d9887-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d9887-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9887-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d9887-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d9887-115">Return code</span></span>                                                                          | <span data-ttu-id="d9887-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9887-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d9887-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d9887-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d9887-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d9887-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d9887-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9887-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9887-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="d9887-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





