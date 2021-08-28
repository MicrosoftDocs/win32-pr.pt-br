---
description: 'Saiba mais sobre: função JET_CALLBACK retorno de chamada'
title: JET_CALLBACK de retorno de chamada
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08d992d1e8b6ca7c6a987a57f44b48d6ba291328
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471162"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK de retorno de chamada


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK de retorno de chamada

A **JET_CALLBACK** é uma função de retorno de chamada de várias finalidades usada pelo mecanismo de banco de dados para informar a aplicação de um evento que envolve desfragmentação online e notificações de estado do cursor.

Consulte [JET_CBTYP](./jet-cbtyp.md) configurações específicas a ser usadas para os parâmetros dessa função, pois essas configurações serão diferentes dependendo da **opção JET_CBTYP** selecionada para uso no parâmetro *cbtyp.*

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão para a qual o retorno de chamada está sendo feito.

*Dbid*

O banco de dados para o qual o retorno de chamada está sendo feito.

*Tableid*

O cursor para o qual o retorno de chamada está sendo feito.

*cbtyp*

O ponto na operação em que o retorno de chamada está sendo feito. Consulte [JET_CBTYP](./jet-cbtyp.md) para ver uma lista de valores e o significado dos parâmetros a seguir em cada caso.

*pvArg1*

Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada com suporte pelo mecanismo de banco de dados.

*pvArg2*

Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada com suporte pelo mecanismo de banco de dados.

*pvContext*

Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada com suporte pelo mecanismo de banco de dados.

*ulUnused*

Um parâmetro usado para se comunicar com o aplicativo usando o retorno de chamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desse parâmetro para cada retorno de chamada com suporte pelo mecanismo de banco de dados.

#### <a name="return-value"></a>Valor Retornado

A função retorna um dos códigos [de erro extensível Armazenamento Mecanismo](./extensible-storage-engine-error-codes.md). Para obter informações sobre como retornar esses códigos como HRESULTs, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md). Em caso de êxito, a operação que emitiu o retorno de chamada pode continuar normalmente. Em alguns casos, o retorno de chamada pode retornar um aviso que influencia essa operação. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso desses avisos pela operação.

Em caso de falha, a operação que emitiu o retorno de chamada pode continuar normalmente ou pode falhar. Consulte [JET_CBTYP](./jet-cbtyp.md) para obter informações sobre o uso do código de erro pela operação.

#### <a name="remarks"></a>Comentários

Se o retorno de chamada passar um cursor para o aplicativo, é importante saber que esse cursor está intencionalmente limitado a um conjunto menor de funcionalidades para evitar a recursão e outras recursões. As seguintes operações são permitidas:

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

Ao projetar o retorno de chamada, leve em conta que, mesmo com essas restrições, ainda é possível que o retorno de chamada falhe.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
