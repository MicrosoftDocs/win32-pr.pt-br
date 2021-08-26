---
description: Evento por usuário gerado na tentativa de baixar arquivos da Web. Esse evento é gerado por aplicativos solicitados pelos Controles dos Pais.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7430b87e7c227fe351e3182f344c60ece0b5a3138b94fe19fee950f96ec24b6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112706"
---
# <a name="wpcevent_web_filedownload-event"></a>Evento WPCEVENT \_ WEB \_ FILEDOWNLOAD

Evento por usuário gerado na tentativa de baixar arquivos da Web. Esse evento é gerado por aplicativos solicitados pelos Controles dos Pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* 
</dt> <dd>

A origem da URL que está tentando baixar.

</dd> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo que está gerando o evento.

</dd> <dt>

*Versão* 
</dt> <dd>

A versão do aplicativo que está gerando o evento.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho de destino para o arquivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




