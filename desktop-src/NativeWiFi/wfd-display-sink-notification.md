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
# <a name="wfd_display_sink_notification-structure"></a>\_Estrutura de \_ notificação do coletor de vídeo WFD \_

A estrutura de **\_ notificação do \_ coletor \_ de vídeo WFD** descreve a notificação passada para a função de retorno de chamada de [**\_ notificação do coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Sintaxe


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



## <a name="members"></a>Membros

<dl> <dt>

**Cabeçalho**
</dt> <dd>

Um [**\_ cabeçalho de \_ \_ objeto do \_ coletor de vídeo WFD**](wfd-display-sink-object-header.md) que descreve os dados incluídos na notificação.

</dd> <dt>

**tipo**
</dt> <dd>

Um valor de [**tipo de notificação do \_ coletor de exibição \_ \_ \_ WFD**](wfd-display-sink-notification-type.md) que indica o tipo da notificação. Esse parâmetro também determina quais informações usar na União abaixo.

</dd> <dt>

**strRemoteDeviceName**
</dt> <dd>

Contém uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo remoto. \_ \_ \_ \_ \_ O comprimento máximo do nome do dispositivo do coletor WFD é definido como o valor (32).

</dd> <dt>

**RemoteDeviceAddress**
</dt> <dd>

Um [**\_ \_ endereço MAC DOT11**](dot11-mac-address-type.md) que contém o bssid do dispositivo remoto.

</dd> <dt>

**ProvisioningRequestInfo**
</dt> <dd>

Informações sobre uma solicitação de provisionamento. Use isto se o *tipo* tiver o valor **ProvisioningRequestNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

O identificador da sessão.

</dd> <dt>

**PossibleConfigMethods**
</dt> <dd>

Métodos possíveis para mostrar a interface do usuário para aceitação interativa.

</dd> </dl> </dd> <dt>

**ReconnectRequestInfo**
</dt> <dd>

Informações sobre uma solicitação de reconexão. Use isto se o *tipo* tiver o valor **ReconnectRequestNotification**.

<dl> <dt>

**GroupID**
</dt> <dd>

A ID do grupo.

</dd> </dl> </dd> <dt>

**ConnectedInfo**
</dt> <dd>

Informações sobre uma notificação conectada. Use isto se o *tipo* tiver o valor **ConnectedNotification**.

<dl> <dt>

**hSessionHandle**
</dt> <dd>

O identificador da sessão.

</dd> <dt>

**guidSessionInterface**
</dt> <dd>

Um GUID que indica a interface da sessão.

</dd> <dt>

**GroupID**
</dt> <dd>

A ID do grupo.

</dd> <dt>

**strProfile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que descreve o perfil.

</dd> <dt>

**LocalAddress**
</dt> <dd>

O endereço local.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

O endereço remoto.

</dd> <dt>

**uRTSPPort**
</dt> <dd>

A porta RTSP.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




