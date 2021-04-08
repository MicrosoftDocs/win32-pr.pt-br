---
description: Cancela a assinatura de notificações de alteração de status do serviço.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Função UnsubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829143"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="39b43-103">Função UnsubscribeServiceChangeNotifications</span><span class="sxs-lookup"><span data-stu-id="39b43-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="39b43-104">Cancela a assinatura de notificações de alteração de status do serviço.</span><span class="sxs-lookup"><span data-stu-id="39b43-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="39b43-105">Essa função usa assinaturas retornadas por [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span><span class="sxs-lookup"><span data-stu-id="39b43-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="39b43-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39b43-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="39b43-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b43-108">*pSubscription* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39b43-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b43-109">Um ponteiro para a assinatura a ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="39b43-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b43-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39b43-110">Return value</span></span>

<span data-ttu-id="39b43-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="39b43-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b43-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="39b43-112">Remarks</span></span>

<span data-ttu-id="39b43-113">**UnsubscribeServiceChangeNotifications** não retorna até que os retornos de chamada em andamento pendentes sejam concluídos.</span><span class="sxs-lookup"><span data-stu-id="39b43-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="39b43-114">Portanto, você não pode chamar **UnsubscribeServiceChangeNotifications** no retorno de chamada sem causar um deadlock.</span><span class="sxs-lookup"><span data-stu-id="39b43-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b43-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39b43-115">Requirements</span></span>



| <span data-ttu-id="39b43-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b43-116">Requirement</span></span> | <span data-ttu-id="39b43-117">Valor</span><span class="sxs-lookup"><span data-stu-id="39b43-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39b43-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39b43-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39b43-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="39b43-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="39b43-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39b43-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39b43-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="39b43-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39b43-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39b43-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b43-123"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b43-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="39b43-124">DLL</span><span class="sxs-lookup"><span data-stu-id="39b43-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b43-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b43-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b43-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="39b43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b43-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="39b43-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="39b43-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="39b43-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="39b43-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="39b43-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="39b43-130">**SubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="39b43-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="39b43-131">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="39b43-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




