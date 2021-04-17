---
description: Define o tipo da notificação passada para a função de \_ retorno de chamada de notificação do coletor de vídeo WFD \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Enumeração de WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748428"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="3a45d-103">\_Enumeração de \_ tipo de notificação do coletor de vídeo WFD \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a45d-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="3a45d-104">O tipo enumerado do **tipo de notificação do \_ coletor de vídeo \_ \_ \_ WFD** define o tipo da notificação passada para a função de retorno de chamada de [**\_ notificação do coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="3a45d-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a45d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a45d-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3a45d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3a45d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3a45d-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="3a45d-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="3a45d-108">A notificação é uma solicitação de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="3a45d-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="3a45d-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="3a45d-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="3a45d-110">A notificação é uma solicitação de reconexão.</span><span class="sxs-lookup"><span data-stu-id="3a45d-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="3a45d-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="3a45d-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="3a45d-112">A notificação é uma notificação conectada.</span><span class="sxs-lookup"><span data-stu-id="3a45d-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="3a45d-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="3a45d-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="3a45d-114">A notificação é uma notificação desconectada.</span><span class="sxs-lookup"><span data-stu-id="3a45d-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a45d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a45d-115">Requirements</span></span>



| <span data-ttu-id="3a45d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a45d-116">Requirement</span></span> | <span data-ttu-id="3a45d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3a45d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a45d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a45d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a45d-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a45d-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3a45d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a45d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a45d-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="3a45d-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3a45d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a45d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a45d-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a45d-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




