---
title: Método IBasicDevice UniqueDeviceName
description: Recupera o nome do dispositivo exclusivo do dispositivo (UDN).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API de streaming de mídia do método UniqueDeviceName
- API de streaming de mídia do método UniqueDeviceName, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364798"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="4e96a-106">Método IBasicDevice:: UniqueDeviceName</span><span class="sxs-lookup"><span data-stu-id="4e96a-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="4e96a-107">Recupera o nome do dispositivo exclusivo do dispositivo (UDN).</span><span class="sxs-lookup"><span data-stu-id="4e96a-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e96a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e96a-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="4e96a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e96a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e96a-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4e96a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e96a-111">Recebe um ponteiro para o modelo s do dispositivo UDN.</span><span class="sxs-lookup"><span data-stu-id="4e96a-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e96a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e96a-112">Return value</span></span>

<span data-ttu-id="4e96a-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4e96a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e96a-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e96a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e96a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4e96a-115">Return code</span></span>                                                                          | <span data-ttu-id="4e96a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e96a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4e96a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e96a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4e96a-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4e96a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4e96a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e96a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e96a-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4e96a-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





