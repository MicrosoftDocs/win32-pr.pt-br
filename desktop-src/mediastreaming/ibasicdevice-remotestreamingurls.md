---
title: Método IBasicDevice RemoteStreamingUrls
description: Retorna um vetor de URLs de streaming remota.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API de streaming de mídia do método RemoteStreamingUrls
- API de streaming de mídia do método RemoteStreamingUrls, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364811"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="d3abd-106">Método IBasicDevice:: RemoteStreamingUrls</span><span class="sxs-lookup"><span data-stu-id="d3abd-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="d3abd-107">Retorna um vetor de URLs de streaming remota.</span><span class="sxs-lookup"><span data-stu-id="d3abd-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3abd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3abd-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="d3abd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3abd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3abd-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d3abd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3abd-111">Recebe uma coleção enumerável de ponteiros para URLs de streaming remota.</span><span class="sxs-lookup"><span data-stu-id="d3abd-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3abd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3abd-112">Return value</span></span>

<span data-ttu-id="d3abd-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d3abd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d3abd-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3abd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d3abd-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d3abd-115">Return code</span></span>                                                                          | <span data-ttu-id="d3abd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3abd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d3abd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3abd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d3abd-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d3abd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d3abd-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3abd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3abd-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="d3abd-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





