---
description: 'Saiba mais sobre: campo Server2003Grbits.ForwardOnly'
title: Campo Server2003Grbits.ForwardOnly (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f98dca3e85eb5ad3c57ef1203971078035c7191ca3e5358dba701dcd870f8480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603836"
---
# <a name="server2003grbitsforwardonly-field"></a>Campo Server2003Grbits.ForwardOnly

Essa opção solicita que a tabela temporária seja criada somente se o gerenciador de tabela temporário puder usar a implementação otimizada para resultados intermediários da consulta. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort. Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte [Exclusivo](./temptablegrbit-enumeration.md) para obter mais informações.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Server2003Grbits](./server2003grbits-class.md)

[Membros de Server2003Grbits](./server2003grbits-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
