---
title: Método de BasicDevice.remove_ConnectionStatusChanged
description: Cancela o registro de um manipulador de eventos para o evento ConnectionStatusChanged. | Método de BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API de streaming de mídia do método remove_ConnectionStatusChanged
- API de streaming de mídia do método remove_ConnectionStatusChanged, interface BasicDevice
- API de streaming de mídia da interface BasicDevice, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172788"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="4a40f-107">Método BasicDevice. Remove \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="4a40f-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="4a40f-108">Cancela o registro de um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4a40f-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a40f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a40f-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="4a40f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a40f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a40f-111">*token* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4a40f-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a40f-112">Uma referência a um token obtido do método [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) quando o manipulador de eventos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="4a40f-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a40f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a40f-113">Return value</span></span>

<span data-ttu-id="4a40f-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4a40f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4a40f-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a40f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4a40f-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4a40f-116">Return code</span></span>                                                                          | <span data-ttu-id="4a40f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a40f-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4a40f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a40f-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4a40f-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4a40f-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4a40f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a40f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a40f-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a40f-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

