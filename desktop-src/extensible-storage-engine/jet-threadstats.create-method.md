---
description: 'Saiba mais sobre: JET_THREADSTATS. Criar método'
title: JET_THREADSTATS. Método Create (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a3450835a90c3e21902a6097d9cfb672c51769cc00810d86e338bef40ce2565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251898"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Criar método

Crie um [novo JET_THREADSTATS](./jet-threadstats-structure2.md) struct com o valor especificado.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>Parâmetros

  - cPageReferenced  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de páginas visitadas.

<!-- end list -->

  - cPageRead  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de páginas lidas.

<!-- end list -->

  - cPagePreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de páginas pré-lidas.

<!-- end list -->

  - cPageDirtied  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de páginas desaginadas.

<!-- end list -->

  - cPageRedirtied  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de páginas redirtidas.

<!-- end list -->

  - cLogRecord  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de registros de log gerados.

<!-- end list -->

  - cbLogRecord  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Bytes de registros de log gravados.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Um novo [JET_THREADSTATS](./jet-threadstats-structure2.md) struct com os valores especificados.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_THREADSTATS estrutura](./jet-threadstats-structure2.md)

[JET_THREADSTATS membros](./jet-threadstats-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
