---
description: 'Saiba mais sobre: método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bf9130715d35fb26b226a2b378f0eba2a853b742ee0a88319ed35f3a121f480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902461"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)

A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. A exclusão de uma linha de tabela é executada chamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão que iniciou a atualização.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor a ser atualizado. Uma atualização deve ser preparada.

<!-- end list -->

  - indicador  
    Escreva \[\]  
    
    Retorna o indicador do registro atualizado. Isso pode ser nulo.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O tamanho do buffer do indicador.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Retorna o tamanho real do indicador.

## <a name="remarks"></a>Comentários

JetUpdate é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e, em seguida, chamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) uma ou mais vezes para definir o estado do registro. Por fim, JetUpdate (JET_SESID, JET_TABLEID, \[ \] Int32, Int32) é chamado para concluir a operação de atualização. Os índices são atualizados somente por JetUpdate ou e não durante o JetSetColumn.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetUpdate](./api.jetupdate-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
