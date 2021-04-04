---
title: Método IBasicDevice ManufacturerUrl
description: Recupera a URL do fabricante do dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- API de streaming de mídia do método ManufacturerUrl
- API de streaming de mídia do método ManufacturerUrl, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006484"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="44cbc-106">Método IBasicDevice:: ManufacturerUrl</span><span class="sxs-lookup"><span data-stu-id="44cbc-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="44cbc-107">Recupera a URL do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44cbc-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="44cbc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44cbc-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="44cbc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44cbc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44cbc-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="44cbc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44cbc-111">Recebe um ponteiro para a URL do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44cbc-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44cbc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44cbc-112">Return value</span></span>

<span data-ttu-id="44cbc-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="44cbc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="44cbc-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="44cbc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="44cbc-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="44cbc-115">Return code</span></span>                                                                          | <span data-ttu-id="44cbc-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="44cbc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="44cbc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="44cbc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="44cbc-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="44cbc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="44cbc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="44cbc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44cbc-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="44cbc-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





