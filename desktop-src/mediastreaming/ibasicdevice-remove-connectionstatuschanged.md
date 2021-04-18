---
title: Método de remove_ConnectionStatusChanged IBasicDevice
description: Cancela o registro de um manipulador de eventos para o evento ConnectionStatusChanged. | Método de remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API de streaming de mídia do método remove_ConnectionStatusChanged
- API de streaming de mídia do método remove_ConnectionStatusChanged, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105764492"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="fa2ba-107">Método IBasicDevice:: Remove \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="fa2ba-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="fa2ba-108">Cancela o registro de um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="fa2ba-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2ba-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa2ba-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="fa2ba-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa2ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa2ba-111">*token* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fa2ba-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa2ba-112">Uma referência a um token obtido do método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando o manipulador de eventos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="fa2ba-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa2ba-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa2ba-113">Return value</span></span>

<span data-ttu-id="fa2ba-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fa2ba-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fa2ba-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa2ba-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fa2ba-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa2ba-116">Return code</span></span>                                                                          | <span data-ttu-id="fa2ba-117">Description</span><span class="sxs-lookup"><span data-stu-id="fa2ba-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fa2ba-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2ba-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fa2ba-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa2ba-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fa2ba-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa2ba-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2ba-121">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="fa2ba-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





