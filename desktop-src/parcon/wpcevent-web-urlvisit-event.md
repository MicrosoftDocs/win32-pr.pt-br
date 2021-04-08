---
description: Evento por usuário gerado pelo filtro de conteúdo da Web devido à tentativa de acessar uma URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010976"
---
# <a name="wpcevent_web_urlvisit-event"></a>\_Evento WPCEVENT Web \_ URLVISIT

Evento por usuário gerado pelo filtro de conteúdo da Web devido à tentativa de acessar uma URL.


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

A cadeia de caracteres da versão para o aplicativo.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

Um GUID que identifica o sistema de classificação atual.

</dd> <dt>

*CatCount* 
</dt> <dd>

A contagem de entradas bloqueadas no campo Categoria.

</dd> <dt>

*Categoria* 
</dt> <dd>

Uma cadeia de caracteres delimitada de identificadores de categoria que são bloqueados.

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

 

 




