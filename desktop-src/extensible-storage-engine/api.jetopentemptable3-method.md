---
description: 'Saiba mais sobre: Método Api.JetOpenTempTable3'
title: Método Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09100f3dcc1165d73e35349b404b78085323743a4d83d269f6f4775dc0b94375
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948036"
---
# <a name="apijetopentemptable3-method"></a>Método Api.JetOpenTempTable3

Cria uma tabela temporária com um único índice. Uma tabela temporária armazena e recupera registros como uma tabela comum criada usando JetCreateTableColumnIndex. No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar a remoção duplicada muito rapidamente em conjuntos de registros quando acessados de maneira puramente sequencial. Consulte [também JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - colunas  
    Tipo: \[\]  
    
    Definições de coluna para as colunas criadas na tabela temporária.

<!-- end list -->

  - numColumns  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de definições de coluna.

<!-- end list -->

  - unicodeindex  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    A ID de localidade e sinalizadores de normalização que serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Quando isso não estiver presente, as opções padrão serão usadas.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Opções de criação de tabela.

<!-- end list -->

  - Tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Retorna a tableid da tabela temporária. Fechar esta tableid com [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera os recursos associados à tabela temporária.

<!-- end list -->

  - Columnids  
    Tipo: \[\]  
    
    O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária. As IDs de coluna nessa matriz corresponderão exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
