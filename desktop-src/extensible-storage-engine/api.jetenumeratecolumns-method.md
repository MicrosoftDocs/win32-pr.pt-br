---
description: 'Saiba mais sobre: método API. JetEnumerateColumns'
title: Método API. JetEnumerateColumns
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010422"
---
# <a name="apijetenumeratecolumns-method"></a>Método API. JetEnumerateColumns

Recupera com eficiência um conjunto de colunas e seus valores do registro atual de um cursor ou o buffer de cópia desse cursor. As colunas e os valores recuperados podem ser restringidos por uma lista de IDs de coluna, números de itagSequence e outras características. Essa API de recuperação de coluna é exclusiva, pois retorna informações na memória alocada dinamicamente que é obtida usando um retorno de chamada compatível de realocação fornecido pelo usuário. Essa nova flexibilidade permite a recuperação eficiente de dados de coluna com características específicas (como tamanho e multiplicidade) que são desconhecidos para o chamador. Isso elimina a necessidade de usar os modos de descoberta de JetRetrieveColumn para determinar essas características a fim de configurar uma chamada final para JetRetrieveColumn que recuperará com êxito os dados desejados.

Esta API não está em conformidade com CLS. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor do qual recuperar dados.

<!-- end list -->

  - numColumnids  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Os números de JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    Escreva \[\]  
    
    Uma matriz opcional de IDs de coluna, cada uma com uma matriz opcional de números itagSequence para enumerar.

<!-- end list -->

  - numColumnValues  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Retorna o número de valores de coluna recuperados.

<!-- end list -->

  - columnValues  
    Escreva \[\]  
    
    Retorna os valores da coluna enumerada.

<!-- end list -->

  - allocator  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Retorno de chamada usado para alocar memória.

<!-- end list -->

  - allocatorContext  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexto para o retorno de chamada de alocação.

<!-- end list -->

  - maxDataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Define um limite na quantidade de dados a serem retornados de uma coluna longa de texto longo ou binário longo. Esse parâmetro pode ser usado para impedir a enumeração de um valor de coluna muito grande.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Recuperar opções.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Um aviso ou sucesso.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
