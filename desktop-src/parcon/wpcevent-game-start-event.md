---
description: Evento por usuário gerado pelo sistema ao tentar iniciar um jogo. Vários valores de campo são fornecidos pelo sistema Do Games Explorer e metadados correspondentes do GDF (Arquivo de Definição de Jogo) fornecidos por jogos com suporte.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41367a47a9bace8dd615ab4b6eea0a875099aab465c285389478c4bee0a39392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951496"
---
# <a name="wpcevent_game_start-event"></a>Evento WPCEVENT \_ GAME \_ START

Evento por usuário gerado pelo sistema ao tentar iniciar um jogo. Vários valores de campo são fornecidos pelo sistema Do Games Explorer e metadados correspondentes do GDF (Arquivo de Definição de Jogo) fornecidos por jogos com suporte.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppID* 
</dt> <dd>

O GUID do jogo que tentou iniciar.

</dd> <dt>

*InstanceID* 
</dt> <dd>

O GUID usado para distinguir entre várias instalações.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A cadeia de caracteres de versão do jogo.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho para o diretório primário da instalação do jogo.

</dd> <dt>

*Classificação* 
</dt> <dd>

Uma cadeia de caracteres que identifica o nível de classificação de um jogo dentro do sistema de classificação.

</dd> <dt>

*RatingSystem* 
</dt> <dd>

Um GUID que identifica o sistema de classificação atual ao qual o nível de classificação se aplica.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*DescCount* 
</dt> <dd>

A contagem de descritores que estão presentes no campo descritor.

</dd> <dt>

*Descritor* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém descritores bloqueados para o jogo.

</dd> <dt>

*Pid* 
</dt> <dd>

A ID do processo do jogo, que é usada para correlacionar com um desligamento de shim do processo.

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

 

 




