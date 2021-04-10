---
title: Método SerialNumber IBasicDevice
description: Recupera o número de série do dispositivo.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- API de streaming de mídia do método SerialNumber
- API de streaming de mídia do método SerialNumber, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293175"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="403e3-106">Método IBasicDevice:: SerialNumber</span><span class="sxs-lookup"><span data-stu-id="403e3-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="403e3-107">Recupera o número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="403e3-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="403e3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="403e3-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="403e3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="403e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403e3-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="403e3-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403e3-111">Recebe um ponteiro para o número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="403e3-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403e3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="403e3-112">Return value</span></span>

<span data-ttu-id="403e3-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="403e3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="403e3-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="403e3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="403e3-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="403e3-115">Return code</span></span>                                                                          | <span data-ttu-id="403e3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="403e3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="403e3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="403e3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="403e3-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="403e3-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="403e3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="403e3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403e3-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="403e3-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





