---
description: 'Saiba mais sobre: método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 50a42d3ca0b1e81dc7f5205482c99a019b4143e5d3f1e6cb8f7cb61c65886f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118271900"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a>Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)

Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor do qual recuperar a coluna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    O columnid a ser recuperado.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Recuperar opções de coluna.

<!-- end list -->

  - retinfo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Se pretinfo for atribuído como NULL, a função se comporta como se um itagSequence de 1 e um ibLongValue de 0 (zero) fossem fornecidos. Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).

#### <a name="return-value"></a>Retornar valor

Escreva \[\]  
Os dados recuperados da coluna. NULL se a coluna for nula.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de RetrieveColumn](./api.retrievecolumn-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
