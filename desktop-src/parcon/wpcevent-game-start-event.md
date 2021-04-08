---
description: Evento por usuário gerado pelo sistema na tentativa de iniciar um jogo. Vários valores de campo são fornecidos pelo sistema do explorador de jogos e pelos metadados de GDF (arquivo de definição de jogo) correspondentes fornecidos por jogos com suporte.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010977"
---
# <a name="wpcevent_game_start-event"></a>Evento de início do \_ jogo WPCEVENT \_

Evento por usuário gerado pelo sistema na tentativa de iniciar um jogo. Vários valores de campo são fornecidos pelo sistema do explorador de jogos e pelos metadados de GDF (arquivo de definição de jogo) correspondentes fornecidos por jogos com suporte.


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

A cadeia de caracteres da versão para o jogo.

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

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*DescCount* 
</dt> <dd>

A contagem de descritores que estão presentes no campo de descritor.

</dd> <dt>

*Descritor* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém descritores que estão bloqueados para o jogo.

</dd> <dt>

*PESSOAL* 
</dt> <dd>

A ID do processo do jogo, que é usada para correlacionar com um desligamento de Shim do processo.

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

 

 




