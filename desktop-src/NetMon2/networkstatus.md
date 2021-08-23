---
description: A estrutura NETWORKSTATUS descreve o status atual do NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Estrutura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3031cd8bd8f1af4e5ea5f03aec93b9a2f28b3ec098a8110563bb89869c97ae3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799516"
---
# <a name="networkstatus-structure"></a>Estrutura NETWORKSTATUS

A estrutura **NETWORKSTATUS** descreve o status atual do NPP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**State**
</dt> <dd>

Indica o estado atual do NPP.



| Valor                                                                                                                                                                                                          | Significado                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS de \_ estado \_ nulo**</dt> </dl>                | O NPP não está conectado ou está conectado e a captura não foi iniciada.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**\_captura de estado NETWORKSTATUS \_**</dt> </dl> | O NPP está capturando dados.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**Estado de NETWORKSTATUS \_ \_ pausado**</dt> </dl>          | O NPP foi pausado durante a captura de dados.<br/>                                     |



 

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Sinalizadores que descrevem o estado atual do NPP.



| Valor                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**\_gatilho de sinalizadores NETWORKSTATUS \_ \_ pendentes**</dt> </dl> | Há um gatilho pendente para o NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao usar essa estrutura, você deve alocar a memória para a estrutura antes que ela possa ser usada e liberar a memória quando a estrutura não for mais necessária.

A lista ver também na parte inferior deste tópico lista todos os métodos que usam essa estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC:: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP:: QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC:: QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats:: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




