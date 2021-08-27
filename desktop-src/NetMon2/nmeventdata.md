---
description: A estrutura NMEVENTDATA contém informações sobre uma condição de evento que é passada para Monitor de Rede inserir uma linha no visualizador especialista.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estrutura NMEVENTDATA (Netmon.h)
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
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037036"
---
# <a name="nmeventdata-structure"></a>Estrutura NMEVENTDATA

A **estrutura NMEVENTDATA** contém informações sobre uma condição de evento que é passada para Monitor de Rede inserir uma linha no visualizador especialista.

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

Número de versão da **estrutura NMEVENTDATA.** O número de versão deve ser zero. Versões futuras do Monitor de Rede podem dar suporte a um número de versão mais alto.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificador do evento. **EventIdent** é exclusivo para cada especialista e faz referência a uma página [de referência de evento](event-reference-page.md).

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um conjunto de sinalizadores que descreve quem envia os dados do evento e como o evento é exibido.



| Valor                                                                                                                                                                                                                                              | Significado                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**ESPECIALISTA EM \_ SINALIZADOR \_ DE EVENTO**</dt> </dl>                                                                         | O evento veio de um especialista. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ NÃO \_ EXIBE \_ \_ GRAVIDADE**</dt> </dl>                 | Não exibir o nível de severidade do evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ NÃO EXIBE A \_ \_ \_ ORIGEM**</dt> </dl>                       | Não exibir o nome de origem do evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ NÃO EXIBE O NOME DO \_ \_ \_ \_ EVENTO**</dt> </dl>          | Não exibir o nome do evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ NÃO EXIBE A \_ \_ \_ DESCRIÇÃO**</dt> </dl>        | Não exibir a descrição do evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ NÃO \_ EXIBIR \_ \_ COMPUTADOR**</dt> </dl>                    | Não exibir o nome do computador para o evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ NÃO EXIBE A \_ \_ \_ HORA**</dt> </dl>                             | Não exibir a hora do evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ NÃO \_ EXIBE \_ \_ \_ COLUNAS FIXAS**</dt> </dl> | Não exibir as colunas Gravidade, Origem, Nome do Evento, Descrição, Computador ou Hora. Esse não é um único sinalizador, mas é uma união dos seis sinalizadores anteriores. <br/> |



 

</dd> <dt>

**Gravidade**
</dt> <dd>

Nível de severidade do evento. O nível de severidade pode ter um dos seguintes valores:

AVISO DE SEVERIDADE NMEVENT INFORMATIVA NMEVENT AVISO DE SEVERIDADE NMEVENT AVISO FORTE DE SEVERIDADE NMEVENT ERRO DE GRAVIDADE NMEVENT ERRO GRAVE DE SEVERIDADE NMEVENT ERRO CRÍTICO DE SEVERIDADE \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ NMEVENT \_ \_ \_

</dd> <dt>

**NumColumns**
</dt> <dd>

Número de colunas designadas na estrutura atual.

</dd> <dt>

**szSourceName**
</dt> <dd>

Nome do especialista que é exibido.

</dd> <dt>

**szEventName**
</dt> <dd>

Nome do evento exibido.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrição do evento exibido.

</dd> <dt>

**szMachine**
</dt> <dd>

Obsoleto, deve ser **NULL.**

</dd> <dt>

**Justificativa**
</dt> <dd>

Informações exibidas na segunda janela do Visualizador de Eventos. O **membro justification** pode ser **NULL.** Se for **NULL,** a segunda janela não estará visível.

</dd> <dt>

**Szurl**
</dt> <dd>

Reservado; esse membro deve ser **NULL.**

</dd> <dt>

**SysTime**
</dt> <dd>

Hora em que a condição do evento ocorre. O tempo é medido em relação ao início da captura.

</dd> <dt>

**Coluna**
</dt> <dd>

Tabela de estruturas de coluna que aparece no painel superior do Visualizador de Eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




