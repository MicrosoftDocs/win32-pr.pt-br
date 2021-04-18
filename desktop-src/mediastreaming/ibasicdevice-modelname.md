---
title: Método ModelName IBasicDevice
description: Recupera o nome do modelo do dispositivo.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API de streaming de mídia do método ModelName
- API de streaming de mídia do método ModelName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105779511"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="c9f0e-106">Método IBasicDevice:: ModelName</span><span class="sxs-lookup"><span data-stu-id="c9f0e-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="c9f0e-107">Recupera o nome do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9f0e-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f0e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9f0e-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="c9f0e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9f0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f0e-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c9f0e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f0e-111">Recebe um ponteiro para o nome do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9f0e-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f0e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9f0e-112">Return value</span></span>

<span data-ttu-id="c9f0e-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9f0e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9f0e-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9f0e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9f0e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c9f0e-115">Return code</span></span>                                                                          | <span data-ttu-id="c9f0e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9f0e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9f0e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f0e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9f0e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c9f0e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c9f0e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9f0e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f0e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="c9f0e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





