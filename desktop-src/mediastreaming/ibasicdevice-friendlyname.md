---
title: Método FriendlyName IBasicDevice
description: Recupera o nome amigável do dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- API de streaming de mídia do método FriendlyName
- API de streaming de mídia do método FriendlyName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638590"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="15be1-106">Método IBasicDevice:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15be1-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="15be1-107">Recupera o nome amigável do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15be1-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="15be1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15be1-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="15be1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15be1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15be1-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="15be1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15be1-111">Recebe um ponteiro para o nome amigável do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15be1-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15be1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15be1-112">Return value</span></span>

<span data-ttu-id="15be1-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="15be1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="15be1-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="15be1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="15be1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="15be1-115">Return code</span></span>                                                                          | <span data-ttu-id="15be1-116">Description</span><span class="sxs-lookup"><span data-stu-id="15be1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="15be1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15be1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="15be1-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="15be1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="15be1-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="15be1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15be1-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="15be1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





