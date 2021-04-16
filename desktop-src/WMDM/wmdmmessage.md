---
title: Enumeração WMDMMessage
description: O tipo de enumeração WMDMMessage define os tipos e os Estados de mensagens.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- WMDMMessage de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789588"
---
# <a name="wmdmmessage-enumeration"></a>Enumeração WMDMMessage

O tipo de enumeração **WMDMMessage** define os tipos e os Estados de mensagens.

## <a name="syntax"></a>Syntax


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_chegada do \_ dispositivo de msg do WMDM \_**
</dt> <dd>

Um dispositivo Windows Media Gerenciador de Dispositivos foi conectado.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_remoção do \_ dispositivo de msg do WMDM \_**
</dt> <dd>

Um dispositivo Windows Media Gerenciador de Dispositivos foi removido.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_chegada de \_ mídia de mensagem WMDM \_**
</dt> <dd>

A mídia foi inserida em um dispositivo Windows Media Gerenciador de Dispositivos.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_remoção de \_ mídia de mensagem WMDM \_**
</dt> <dd>

A mídia foi removida de um dispositivo Windows Media Gerenciador de Dispositivos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





