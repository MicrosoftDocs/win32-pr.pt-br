---
title: Método IBasicDevice ModelUrl
description: Recupera a URL do modelo do dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API de streaming de mídia do método ModelUrl
- API de streaming de mídia do método ModelUrl, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293163"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="24335-106">Método IBasicDevice:: ModelUrl</span><span class="sxs-lookup"><span data-stu-id="24335-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="24335-107">Recupera a URL do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24335-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="24335-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24335-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="24335-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24335-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24335-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="24335-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24335-111">Recebe um ponteiro para a URL do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24335-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24335-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24335-112">Return value</span></span>

<span data-ttu-id="24335-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="24335-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="24335-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="24335-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="24335-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="24335-115">Return code</span></span>                                                                          | <span data-ttu-id="24335-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="24335-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="24335-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24335-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="24335-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="24335-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="24335-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="24335-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24335-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="24335-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





