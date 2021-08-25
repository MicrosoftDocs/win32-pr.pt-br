---
title: Enumeração WMDMMessage
description: O tipo de enumeração WMDMMessage define tipos e estados de mensagem.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Janelas de enumeração WMDMMessage Gerenciador de Dispositivos
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
ms.openlocfilehash: 348092e079428e0b147d8143411cee7766365913115f968ed0e112b209383077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862656"
---
# <a name="wmdmmessage-enumeration"></a>Enumeração WMDMMessage

O **tipo de enumeração WMDMMessage** define tipos e estados de mensagem.

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

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**CHEGADA DO DISPOSITIVO \_ WMDM MSG \_ \_**
</dt> <dd>

Um Windows mídia Gerenciador de Dispositivos dispositivo foi conectado.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**REMOÇÃO DE \_ DISPOSITIVO MSG \_ DO WMDM \_**
</dt> <dd>

Um Windows mídia Gerenciador de Dispositivos foi removido.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**CHEGADA DA MÍDIA \_ MSG \_ DO WMDM \_**
</dt> <dd>

A mídia foi inserida em um Windows mídia Gerenciador de Dispositivos dispositivo.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**REMOÇÃO DE \_ MÍDIA MSG \_ DO WMDM \_**
</dt> <dd>

A mídia foi removida de um Windows mídia Gerenciador de Dispositivos dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





