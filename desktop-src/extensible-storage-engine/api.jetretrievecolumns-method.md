---
description: 'Saiba mais sobre: Método Api.JetRetrieveColumns'
title: Método Api.JetRetrieveColumns
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be958a40b4d5617d7c972933e472d911c96d481d7d020f082c5b063281e7d879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840696"
---
# <a name="apijetretrievecolumns-method"></a>Método Api.JetRetrieveColumns

Recupera vários valores de coluna do registro atual em uma única operação. Uma matriz de JET_RETRIEVECOLUMN estruturas é usada para descrever o conjunto de valores de coluna a serem recuperados e para descrever buffers de saída para cada valor de coluna a ser recuperado.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor do onde recuperar os dados.

<!-- end list -->

  - retrievecolumns  
    Tipo: \[\]  
    
    Uma matriz de um ou [mais JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objetos que descrevem os dados a serem recuperados.

<!-- end list -->

  - numColumns  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O número de entradas na matriz de colunas.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Se qualquer coluna recuperada for truncada devido a um buffer de comprimento insuficiente, a API retornará [BufferTruncado.](./jet-wrn-enumeration.md) No entanto, outros JET_wrnColumnNull são retornados somente no campo de erro do [objeto JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objeto .  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
