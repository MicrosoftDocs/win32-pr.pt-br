---
title: UUID
description: Fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada do gerenciador ou um objeto cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925943"
---
# <a name="uuid-structure"></a>Estrutura UUID

A **estrutura UUID** define um UUID (Identificador Universal Exclusivo). Um **UUID** fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada do gerenciador ou um objeto cliente.

A **estrutura UUID** é um `typedef` sinônimo 'd para a estrutura [GUID.](/windows/win32/api/guiddef/ns-guiddef-guid)

## <a name="syntax"></a>Sintaxe

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Comentários

As bibliotecas de tempo de execução RPC usam **UUIDs** para verificar a compatibilidade entre clientes e servidores e selecionar entre várias implementações de uma interface.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | Definido em rpcdce.h; include rpc.h |

## <a name="see-also"></a>Confira também

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)