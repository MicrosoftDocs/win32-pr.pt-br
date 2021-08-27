---
description: 'Saiba mais sobre: Função JetGetColumnInfo'
title: Função JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97b6dfc76de520249880314ecd32769951c7b927
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479102"
---
# <a name="jetgetcolumninfo-function"></a>Função JetGetColumnInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetcolumninfo-function"></a>Função JetGetColumnInfo

A **função JetGetColumnInfo** recupera informações sobre uma coluna.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Dbid*

Identifica, juntamente com *szTableName*, a tabela que contém a coluna da qual as informações são recuperadas.

*szTableName*

Identifica, juntamente com *dbid*, a tabela que contém a coluna da qual as informações são recuperadas.

*szColumnName*

O nome da coluna para a que as informações são buscadas.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer depende de *InfoLevel.* O chamador deve ser configurado para alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult.*

*InfoLevel*

O tipo de informação a ser recuperado para a coluna especificada por *szColumnName*. O formato dos dados armazenados *em pvResult* depende desse parâmetro. Para o esquema da tabela temporária, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

Esses *InfoLevels* são diferenciados por:

  - JET_ColInfoListSortColumnid classificará a tabela temporária por *columnid*.

  - JET_ColInfoListCompact compactar a saída. Para obter mais informações sobre a saída compacta, [consulte JET_COLUMNLIST](./jet-columnlist-structure.md).

As opções a seguir estão disponíveis para uso com esse parâmetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações. <em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> é interpretado como uma estrutura <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> dados. Isso é semelhante a uma <a href="gg294130(v=exchg.10).md">estrutura JET_COLUMNDEF</a> dados. Se essa função for bem-sucedida, a estrutura será populada com os valores apropriados. Se essa função falhar, a estrutura conterá dados indefinido.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Assim como JET_ColInfo, <em>pvResult</em> é interpretado como um JET_COLUMNDEF , exceto que esse <em>InfoLevel</em> indica que <a href="gg294130(v=exchg.10).md">a</a>coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> é interpretado como uma <a href="gg269228(v=exchg.10).md">estrutura JET_COLUMNLIST</a> dados. Se essa função for bem-sucedida, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e é identificada pelo membro <strong>tableid</strong> da <a href="gg269228(v=exchg.10).md">estrutura JET_COLUMNLIST.</a> A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Se essa função falhar, a estrutura conterá dados indefinido.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>O mesmo que JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>O mesmo que JET_ColInfoList; no entanto, a tabela resultante é classificação por columnid, em vez do nome da coluna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor é preterido e o uso dele retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Assim como JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que <em>esse InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> Esse valor é introduzido no Windows Vista.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Retornar somente colunas não derivadas (se a tabela for derivada de um modelo).</p><p>Esse valor pode ser logicamente ou 'd no <em>InfoLevel</em>, quando o <em>InfoLevel</em> base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Esse valor é introduzido Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Retorna apenas o nome da coluna e columnid de cada coluna.</p><p>Esse valor pode ser logicamente ou 'd no <em>InfoLevel</em>, quando o <em>InfoLevel</em> base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Esse valor é introduzido no Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Classificar lista de colunas retornadas por columnid (o padrão é classificar lista por nome de coluna).</p><p>Esse valor pode ser logicamente ou 'd no <em>InfoLevel</em>, quando o <em>InfoLevel</em> base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Esse valor é introduzido no Windows Vista.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errColumnNotFound</p> | <p>A coluna chamada <em>szColumnName</em> não foi encontrada na tabela.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Um <em>InfoLevel ruim</em> foi especificado.</p> | 
| <p>JET_errInvalidName</p> | <p>Esse erro poderá ser retornado se:</p><ul><li><p>Um nome ruim para <em>szTableName</em> foi dado.</p></li><li><p>Um nome ruim para <em>szColumnName</em> foi dado.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Esse erro poderá ser retornado se:</p><ul><li><p>Um <em>InfoLevel ruim</em> foi especificado.</p></li><li><p>Um null <em>szTableName</em> foi passado.</p></li><li><p>O buffer é muito pequeno.</p></li></ul> | 



#### <a name="remarks"></a>Comentários

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) e **JetGetColumnInfo** recuperam informações sobre uma coluna. A diferença entre eles é como a tabela é identificada:

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica uma tabela por *tableid*.

  - **JetGetColumnInfo** identifica uma tabela por *combinação dbid* e *szTableName.*

Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta. A tabela temporária contém dados e a [estrutura JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para percorrer a tabela temporária. A tabela temporária deve ser fechada com [JetCloseTable.](./jetclosetable-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetColumnInfoW</strong> (Unicode) e <strong>JetGetColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
