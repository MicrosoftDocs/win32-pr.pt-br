---
description: 'Saiba mais sobre: JET_CALLBACK delegado'
title: JET_CALLBACK delegado
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ba54414bcc7043edb06300b7bda31e40b838cbc6f78f32171f26c1e37684c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487302"
---
# <a name="jet_callback-delegate"></a>JET_CALLBACK delegado

Uma função de retorno de chamada de várias finalidades usada pelo mecanismo de banco de dados para informar o aplicativo de um evento que envolve a desfragmentação online e notificações de estado do cursor.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão para a qual o retorno de chamada está sendo feito.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    O banco de dados para o qual o retorno de chamada está sendo feito.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor para o qual o retorno de chamada está sendo feito.

<!-- end list -->

  - cbtyp  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    A operação para a qual o retorno de chamada está sendo feito.

<!-- end list -->

  - arg1  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Primeiro argumento específico de retorno de chamada.

<!-- end list -->

  - arg2  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Segundo argumento específico de retorno de chamada.

<!-- end list -->

  - contexto  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexto de retorno de chamada.

<!-- end list -->

  - unused  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Este parâmetro não é usado.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
