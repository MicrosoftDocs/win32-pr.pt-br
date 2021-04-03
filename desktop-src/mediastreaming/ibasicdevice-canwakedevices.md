---
title: Método IBasicDevice CanWakeDevices
description: Recupera um valor que indica se o dispositivo pode ser ativado.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API de streaming de mídia do método CanWakeDevices
- API de streaming de mídia do método CanWakeDevices, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006612"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="544b2-106">Método IBasicDevice:: CanWakeDevices</span><span class="sxs-lookup"><span data-stu-id="544b2-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="544b2-107">Recupera um valor que indica se o dispositivo pode ser ativado.</span><span class="sxs-lookup"><span data-stu-id="544b2-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="544b2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="544b2-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="544b2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="544b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="544b2-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="544b2-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="544b2-111">Recebe um ponteiro para um valor booliano que é **verdadeiro** se o dispositivo puder ser ativado.</span><span class="sxs-lookup"><span data-stu-id="544b2-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="544b2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="544b2-112">Return value</span></span>

<span data-ttu-id="544b2-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="544b2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="544b2-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="544b2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="544b2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="544b2-115">Return code</span></span>                                                                          | <span data-ttu-id="544b2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="544b2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="544b2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="544b2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="544b2-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="544b2-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="544b2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="544b2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544b2-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="544b2-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





