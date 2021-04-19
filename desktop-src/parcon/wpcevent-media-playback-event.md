---
description: Evento por usuário gerado por uma tentativa de reproduzir conteúdo com um aplicativo de mídia conectado aos controles dos pais.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: WPCEVENT_MEDIA_PLAYBACK evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105793859"
---
# <a name="wpcevent_media_playback-event"></a>Evento de reprodução de \_ mídia do WPCEVENT \_

Evento por usuário gerado por uma tentativa de reproduzir conteúdo com um aplicativo de mídia conectado aos controles dos pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo de mídia que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A versão do aplicativo de mídia que está gerando o evento.

</dd> <dt>

*MediaType* 
</dt> <dd>

Um valor da enumeração [**de \_ \_ tipo de mídia WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) que indica informações sobre o tipo de arquivo de mídia acessado.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho para a origem do conteúdo de mídia.

</dd> <dt>

*Título* 
</dt> <dd>

Os metadados do título para o conteúdo.

</dd> <dt>

*PML* 
</dt> <dd>

O nível de gerenciamento de pais.

</dd> <dt>

*Álbuns* 
</dt> <dd>

Os metadados do álbum para o conteúdo.

</dd> <dt>

*Explicita* 
</dt> <dd>

Um valor da enumeração [**de \_ mídia \_ explícita do wpc**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) que indica informações sobre a classificação explícita do arquivo de mídia.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

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

 

 




