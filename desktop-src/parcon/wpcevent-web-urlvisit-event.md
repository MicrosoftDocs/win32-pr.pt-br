---
description: Evento por usuário gerado pelo Filtro de Conteúdo da Web devido à tentativa de acessar uma URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9524909ee78d14395e2f208fe265b3abc31240d2036788b8b84c4fea05aac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112696"
---
# <a name="wpcevent_web_urlvisit-event"></a>Evento WPCEVENT \_ WEB \_ URLVISIT

Evento por usuário gerado pelo Filtro de Conteúdo da Web devido à tentativa de acessar uma URL.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* 
</dt> <dd>

A URL que está tentando ser aberta.

</dd> <dt>

*Aplicativo* 
</dt> <dd>

O aplicativo que está gerando o evento.

</dd> <dt>

*Versão* 
</dt> <dd>

A cadeia de caracteres de versão do aplicativo.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

Um GUID que identifica o sistema de classificação atual.

</dd> <dt>

*CatCount* 
</dt> <dd>

A contagem de entradas bloqueadas no campo de categoria.

</dd> <dt>

*Categoria* 
</dt> <dd>

Uma cadeia de caracteres delimitada de identificadores de categoria bloqueados.

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

 

 




