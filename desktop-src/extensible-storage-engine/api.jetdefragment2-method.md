---
description: 'Saiba mais sobre: método API. JetDefragment2'
title: Método API. JetDefragment2
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793865"
---
# <a name="apijetdefragment2-method"></a>Método API. JetDefragment2

Inicia e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada para a chamada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    O banco de dados a ser desfragmentado.

<!-- end list -->

  - tableName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Parâmetro não utilizado. A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.

<!-- end list -->

  - passa  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o número máximo de passagens de desfragmentação. Ao parar uma tarefa de desfragmentação online, esse parâmetro é definido como o número de passagens executadas.

<!-- end list -->

  - segundos  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o tempo máximo para a desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido com o período de tempo usado para desfragmentação.

<!-- end list -->

  - retorno de chamada  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Função de retorno de chamada que a desfragmentação usa para relatar o progresso.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. DefragGrbit](./defraggrbit-enumeration.md)  
    
    Opções de desfragmentação.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Um código de aviso.  

## <a name="remarks"></a>Comentários

O retorno de chamada passado para JetDefragment2 pode ser executado de forma assíncrona. O GC não sabe que o código não gerenciado tem uma referência ao retorno de chamada, portanto, é importante garantir que o retorno de chamada não seja coletado.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
