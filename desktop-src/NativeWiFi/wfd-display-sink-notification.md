---
description: Descreve a notificação passada para a \_ função de retorno de chamada de notificação do coletor de vídeo WFD \_ \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Estrutura de WFD_DISPLAY_SINK_NOTIFICATION (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754628"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="7477b-103">\_Estrutura de \_ notificação do coletor de vídeo WFD \_</span><span class="sxs-lookup"><span data-stu-id="7477b-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="7477b-104">A estrutura de **\_ notificação do \_ coletor \_ de vídeo WFD** descreve a notificação passada para a função de retorno de chamada de [**\_ notificação do coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="7477b-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7477b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7477b-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="7477b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7477b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7477b-107">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="7477b-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-108">Um [**\_ cabeçalho de \_ \_ objeto do \_ coletor de vídeo WFD**](wfd-display-sink-object-header.md) que descreve os dados incluídos na notificação.</span><span class="sxs-lookup"><span data-stu-id="7477b-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-109">**tipo**</span><span class="sxs-lookup"><span data-stu-id="7477b-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-110">Um valor de [**tipo de notificação do \_ coletor de exibição \_ \_ \_ WFD**](wfd-display-sink-notification-type.md) que indica o tipo da notificação.</span><span class="sxs-lookup"><span data-stu-id="7477b-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="7477b-111">Esse parâmetro também determina quais informações usar na União abaixo.</span><span class="sxs-lookup"><span data-stu-id="7477b-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-112">**strRemoteDeviceName**</span><span class="sxs-lookup"><span data-stu-id="7477b-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-113">Contém uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="7477b-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="7477b-114">\_ \_ \_ \_ \_ O comprimento máximo do nome do dispositivo do coletor WFD é definido como o valor (32).</span><span class="sxs-lookup"><span data-stu-id="7477b-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="7477b-115">**RemoteDeviceAddress**</span><span class="sxs-lookup"><span data-stu-id="7477b-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-116">Um [**\_ \_ endereço MAC DOT11**](dot11-mac-address-type.md) que contém o bssid do dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="7477b-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-117">**ProvisioningRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="7477b-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-118">Informações sobre uma solicitação de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="7477b-118">Info about a provisioning request.</span></span> <span data-ttu-id="7477b-119">Use isto se o *tipo* tiver o valor **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="7477b-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="7477b-120">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="7477b-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-121">O identificador da sessão.</span><span class="sxs-lookup"><span data-stu-id="7477b-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-122">**PossibleConfigMethods**</span><span class="sxs-lookup"><span data-stu-id="7477b-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-123">Métodos possíveis para mostrar a interface do usuário para aceitação interativa.</span><span class="sxs-lookup"><span data-stu-id="7477b-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7477b-124">**ReconnectRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="7477b-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-125">Informações sobre uma solicitação de reconexão.</span><span class="sxs-lookup"><span data-stu-id="7477b-125">Info about a reconnect request.</span></span> <span data-ttu-id="7477b-126">Use isto se o *tipo* tiver o valor **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="7477b-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="7477b-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="7477b-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-128">A ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="7477b-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7477b-129">**ConnectedInfo**</span><span class="sxs-lookup"><span data-stu-id="7477b-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-130">Informações sobre uma notificação conectada.</span><span class="sxs-lookup"><span data-stu-id="7477b-130">Info about a connected notification.</span></span> <span data-ttu-id="7477b-131">Use isto se o *tipo* tiver o valor **ConnectedNotification**.</span><span class="sxs-lookup"><span data-stu-id="7477b-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="7477b-132">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="7477b-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-133">O identificador da sessão.</span><span class="sxs-lookup"><span data-stu-id="7477b-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-134">**guidSessionInterface**</span><span class="sxs-lookup"><span data-stu-id="7477b-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-135">Um GUID que indica a interface da sessão.</span><span class="sxs-lookup"><span data-stu-id="7477b-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="7477b-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-137">A ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="7477b-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-138">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="7477b-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-139">Um ponteiro para uma cadeia de caracteres terminada em nulo que descreve o perfil.</span><span class="sxs-lookup"><span data-stu-id="7477b-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="7477b-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-141">O endereço local.</span><span class="sxs-lookup"><span data-stu-id="7477b-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="7477b-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-143">O endereço remoto.</span><span class="sxs-lookup"><span data-stu-id="7477b-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="7477b-144">**uRTSPPort**</span><span class="sxs-lookup"><span data-stu-id="7477b-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="7477b-145">A porta RTSP.</span><span class="sxs-lookup"><span data-stu-id="7477b-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7477b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7477b-146">Requirements</span></span>



| <span data-ttu-id="7477b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7477b-147">Requirement</span></span> | <span data-ttu-id="7477b-148">Valor</span><span class="sxs-lookup"><span data-stu-id="7477b-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7477b-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7477b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7477b-150">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7477b-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7477b-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7477b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7477b-152">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="7477b-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7477b-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7477b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7477b-154"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="7477b-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




