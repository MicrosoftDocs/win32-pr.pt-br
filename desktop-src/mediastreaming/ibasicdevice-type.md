---
title: Método de tipo IBasicDevice
description: Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- API de streaming de mídia do método de tipo
- API de streaming de mídia do método de tipo, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método Type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366896"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="88a3e-106">Método IBasicDevice:: Type</span><span class="sxs-lookup"><span data-stu-id="88a3e-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="88a3e-107">Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="88a3e-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="88a3e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88a3e-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="88a3e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88a3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a3e-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="88a3e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88a3e-111">Recebe um ponteiro para um valor [**DeviceTypes**](devicetypes.md) .</span><span class="sxs-lookup"><span data-stu-id="88a3e-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a3e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88a3e-112">Return value</span></span>

<span data-ttu-id="88a3e-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="88a3e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="88a3e-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="88a3e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="88a3e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="88a3e-115">Return code</span></span>                                                                          | <span data-ttu-id="88a3e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="88a3e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="88a3e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88a3e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="88a3e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="88a3e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="88a3e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="88a3e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a3e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="88a3e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





