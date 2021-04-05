---
description: A estrutura NMEVENTDATA contém informações sobre uma condição de evento que é passada para Monitor de Rede para inserir uma linha no Visualizador de especialistas.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estrutura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827345"
---
# <a name="nmeventdata-structure"></a>Estrutura NMEVENTDATA

A estrutura **NMEVENTDATA** contém informações sobre uma condição de evento que é passada para monitor de rede para inserir uma linha no Visualizador de especialistas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

Número de versão da estrutura **NMEVENTDATA** . O número de versão deve ser zero. Versões futuras do Monitor de Rede podem dar suporte a um número de versão mais alto.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificador do evento. **EventIdent** é exclusivo para cada especialista e faz referência a uma [página de referência de evento](event-reference-page.md).

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um conjunto de sinalizadores que descreve quem envia os dados do evento e como o evento é exibido.



| Valor                                                                                                                                                                                                                                              | Significado                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**\_especialista em sinalizador de eventos \_**</dt> </dl>                                                                         | O evento provém de um especialista. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ severidade**</dt> </dl>                 | Não exiba o nível de severidade do evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ origem**</dt> </dl>                       | Não exiba o nome de origem do evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ nome do evento \_**</dt> </dl>          | Não exiba o nome do evento para o evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ Descrição**</dt> </dl>        | Não exiba a descrição do evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ computador**</dt> </dl>                    | Não exiba o nome do computador para o evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ não \_ \_ Exibir \_ hora**</dt> </dl>                             | Não exibir a hora do evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ \_ não \_ exibem \_ colunas fixas \_**</dt> </dl> | Não exiba as colunas gravidade, origem, nome do evento, descrição, máquina ou hora. Isso não é um sinalizador único, mas é uma União dos seis sinalizadores anteriores. <br/> |



 

</dd> <dt>

**Gravidade**
</dt> <dd>

Nível de severidade do evento. O nível de severidade pode ter um dos seguintes valores:

NMEVENT \_ severidade \_ informativa NMEVENT aviso de severidade \_ \_ NMEVENT \_ severidade \_ forte \_ aviso NMEVENT erro de severidade \_ \_ NMEVENT \_ gravidade \_ grave \_ erro NMEVENT \_ gravidade \_ crítica \_ erro

</dd> <dt>

**NumColumns**
</dt> <dd>

Número de colunas designadas na estrutura atual.

</dd> <dt>

**szSourceName**
</dt> <dd>

Nome do especialista exibido.

</dd> <dt>

**szEventName**
</dt> <dd>

Nome do evento que é exibido.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrição do evento que é exibido.

</dd> <dt>

**szMachine**
</dt> <dd>

Obsoleto, deve ser **nulo**.

</dd> <dt>

**Justificativa**
</dt> <dd>

Informações exibidas na segunda janela do Visualizador de Eventos. O membro de **justificativa** pode ser **nulo**. Se for **NULL**, a segunda janela não estará visível.

</dd> <dt>

**szUrl**
</dt> <dd>

Reservado Este membro deve ser **nulo**.

</dd> <dt>

**SysTime**
</dt> <dd>

Hora em que a condição de evento ocorre. O tempo é medido em relação ao início da captura.

</dd> <dt>

**Coluna**
</dt> <dd>

Tabela de estruturas de coluna que aparece no painel superior da Visualizador de Eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




