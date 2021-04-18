---
description: Evento por usuário gerado na tentativa de baixar arquivos da Web. Esse evento é gerado por aplicativos solicitados pelos controles dos pais.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780388"
---
# <a name="wpcevent_web_filedownload-event"></a>\_Evento WPCEVENT Web \_ FileDownload

Evento por usuário gerado na tentativa de baixar arquivos da Web. Esse evento é gerado por aplicativos solicitados pelos controles dos pais.


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

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho de destino para o arquivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




