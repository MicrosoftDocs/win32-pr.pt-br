---
title: Método de descrição de IBasicDevice
description: Recupera uma descrição do dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- API de streaming de mídia do método de descrição
- API de streaming de mídia do método de descrição, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método de descrição
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006418"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="08917-106">IBasicDevice: método descrição de:D</span><span class="sxs-lookup"><span data-stu-id="08917-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="08917-107">Recupera uma descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08917-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="08917-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08917-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="08917-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08917-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08917-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="08917-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08917-111">Recebe um ponteiro para a descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08917-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08917-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08917-112">Return value</span></span>

<span data-ttu-id="08917-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="08917-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="08917-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="08917-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="08917-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="08917-115">Return code</span></span>                                                                          | <span data-ttu-id="08917-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="08917-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="08917-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08917-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="08917-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="08917-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="08917-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="08917-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08917-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="08917-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





