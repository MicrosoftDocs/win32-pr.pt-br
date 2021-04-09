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
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920472"
---
# <a name="etweventwritefull-function"></a>Função EtwEventWriteFull

[A função EtwEventWriteFull e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.]

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

*EventDescriptor* 
</dt> <dd>

Descritor de evento do evento a ser registrada.

</dd> <dt>

*EventProperty*
</dt> <dd>

Sinalizador fornecido pelo usuário.

</dd> <dt>

*ActivityId*
</dt> <dd>

ID da atividade.

</dd> <dt>

*RelatedActivityId*
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

## <a name="return-value"></a>Retornar valor

Um código de erro Win32.

## <a name="remarks"></a>Comentários

A função EtwEventWriteFull e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra. Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas em vez disso.


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | ntetw. h |

## <a name="see-also"></a>Confira também

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
