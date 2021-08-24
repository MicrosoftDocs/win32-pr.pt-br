---
description: Grava um evento completo em uma sessão.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 1fd25931e6a58b97e052ecd7da43bd651688d2bf726d8b5ba2acd84ce820be7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653425"
---
# <a name="etweventwritefull-function"></a>Função EtwEventWriteFull

[A função EtwEventWriteFull e as estruturas retornadas são internas ao sistema operacional e estão sujeitas a alterações de uma versão de Windows para outra.]

Grava um evento completo em uma sessão.

## <a name="syntax"></a>Sintaxe

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RegHandle*
</dt> <dd>

RegHandle para o provedor.

</dd> <dt>

*Eventdescriptor* 
</dt> <dd>

Descritor de evento do evento a ser log.

</dd> <dt>

*EventProperty*
</dt> <dd>

Sinalizador dado pelo usuário.

</dd> <dt>

*ActivityId*
</dt> <dd>

ID da atividade.

</dd> <dt>

*Relatedactivityid*
</dt> <dd>

ID da atividade relacionada.

</dd> <dt>

*UserDataCount*
</dt> <dd>

O número de itens de dados do usuário.

</dd> <dt>

*UserData*
</dt> <dd>

Ponteiro para uma matriz de itens de dados do usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um código de erro Win32.

## <a name="remarks"></a>Comentários

A função EtwEventWriteFull e as estruturas retornadas são internas ao sistema operacional e estão sujeitas a alterações de uma versão de Windows para outra. Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas.


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | ntetw.h |

## <a name="see-also"></a>Confira também

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
