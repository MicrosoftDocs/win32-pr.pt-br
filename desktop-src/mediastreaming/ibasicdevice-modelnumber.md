---
title: Método IBasicDevice ModelNumber
description: Recupera o número do modelo do dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API de streaming de mídia do método ModelNumber
- API de streaming de mídia do método ModelNumber, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823227"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="85526-106">Método IBasicDevice:: ModelNumber</span><span class="sxs-lookup"><span data-stu-id="85526-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="85526-107">Recupera o número do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85526-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="85526-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85526-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="85526-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85526-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85526-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="85526-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85526-111">Recebe um ponteiro para o número do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85526-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85526-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85526-112">Return value</span></span>

<span data-ttu-id="85526-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="85526-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="85526-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="85526-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="85526-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="85526-115">Return code</span></span>                                                                          | <span data-ttu-id="85526-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="85526-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="85526-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="85526-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="85526-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="85526-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="85526-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="85526-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85526-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="85526-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





