---
UID: ''
title: Função InterlockedPushListSList
description: Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2020
ms.locfileid: "104365768"
---
# <a name="interlockedpushlistslist-function"></a>Função InterlockedPushListSList

## <a name="description"></a>Description

Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.
O acesso às listas é sincronizado em um sistema multiprocessador.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Parâmetros

### <a name="listhead-in-out"></a>ListHead [in, out]

Ponteiro para uma estrutura de **SLIST_HEADER** que representa o cabeçalho de uma lista vinculada individualmente.
A lista especificada pela *lista* e parâmetros *escutados* é inserida na frente desta lista.

### <a name="list-in-out"></a>Listar [entrada, saída]

Ponteiro para uma estrutura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa o primeiro item da lista a ser inserida.

### <a name="listend-in-out"></a>Escutado [in, out]

Ponteiro para uma estrutura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa o último item da lista a ser inserido.

### <a name="count-in"></a>Contagem [em]

O número de itens na lista a ser inserido.

## <a name="returns"></a>Retornos

O valor de retorno é o primeiro item anterior na lista especificada pelo parâmetro *ListHead* .
Se a lista estava vazia anteriormente, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Todos os itens de lista devem ser alinhados em um limite de **MEMORY_ALLOCATION_ALIGNMENT** ; caso contrário, essa função terá um comportamento não previsível.
Consulte **_aligned_malloc**.

**Windows 8 e Windows Server 2012:**  Essa função foi substituída por [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).
Ao compilar com **NTDDI_VERSION** definido como **NTDDI_WIN8** ou superior, chamadas para **InterlockedPushListSList** vão para **InterlockedPushListSListEx** em vez disso.

## <a name="see-also"></a>Confira também

[Listas vinculadas isoladamente interbloqueadas](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Usando listas vinculadas individualmente](/windows/desktop/Sync/using-singly-linked-lists)
