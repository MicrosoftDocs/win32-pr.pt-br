---
title: UUID
description: Fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada de gerente ou um objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084253"
---
# <a name="uuid-structure"></a>Estrutura UUID

A estrutura **UUID** define um UUID (identificador universal exclusivo). Um **UUID** fornece uma designação exclusiva de um objeto, como uma interface, um vetor de ponto de entrada de gerente ou um objeto de cliente.

A estrutura do **UUID** é um `typedef` sinônimo para a estrutura de [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .

## <a name="syntax"></a>Sintaxe

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Comentários

As bibliotecas de tempo de execução RPC usam **UUID** s para verificar a compatibilidade entre clientes e servidores e para selecionar entre várias implementações de uma interface.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | Definido em rpcdce. h; incluir RPC. h |

## <a name="see-also"></a>Confira também

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 do [UUID \_ VETOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)