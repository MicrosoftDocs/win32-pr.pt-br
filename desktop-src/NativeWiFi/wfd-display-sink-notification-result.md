---
description: Descreve o resultado que você pode definir opcionalmente depois de processar um coletor de exibição notificação na \_ função de retorno de chamada de notificação do coletor de vídeo WFD \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Estrutura de WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
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
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780076"
---
# <a name="wfd_display_sink_notification_result-structure"></a>\_Estrutura de \_ resultados da notificação do coletor de vídeo WFD \_ \_

A estrutura de **resultados da notificação do \_ coletor de vídeo \_ \_ \_ WFD** descreve o resultado que você pode definir opcionalmente após o processamento de um coletor de vídeo notificação na função de retorno de chamada de [**\_ notificação do coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Cabeçalho**
</dt> <dd>

Um [**\_ cabeçalho de \_ \_ objeto do \_ coletor de vídeo WFD**](wfd-display-sink-object-header.md) que descreve os dados incluídos no resultado da notificação.

</dd> <dt>

**tipo**
</dt> <dd>

Um valor de [**tipo de notificação do \_ coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-type.md) que indica o tipo do resultado da notificação. Esse parâmetro também determina quais informações usar na União abaixo.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Informações sobre o resultado de uma solicitação de provisionamento. Use isto se o *tipo* tiver o valor **ProvisioningRequestNotification**.

<dl> <dt>

**ConfigMethod**
</dt> <dd>

O método para mostrar a interface do usuário para aceitação interativa.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

O número de caracteres largos na *chave* de acesso, não contando nenhum terminador nulo.

</dd> <dt>

**Chave**
</dt> <dd>

Contém a chave de passagem como uma matriz de caracteres largos. \_ \_ \_ \_ \_ \_ O comprimento máximo de chave de acesso de informações do WPS do coletor WFD é definido como o valor (8).

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Informações sobre o resultado de uma solicitação de reconexão. Use isto se o *tipo* tiver o valor **ReconnectRequestNotification**.

<dl> <dt>

**strProfile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que descreve o perfil.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




