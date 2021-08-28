---
description: 'Saiba mais sobre: função JetGetColumnInfo'
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
ms.openlocfilehash: e7f3473f15682196f1557810ce4e1d4df3d09aaa
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983639"
---
# <a name="jetgetcolumninfo-function"></a>Função JetGetColumnInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetcolumninfo-function"></a>Função JetGetColumnInfo

A função **JetGetColumnInfo** recupera informações sobre uma coluna.

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

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

Identifica, juntamente com *szTableName*, a tabela que contém a coluna da qual as informações são recuperadas.

*szTableName*

Identifica, juntamente com *DBID*, a tabela que contém a coluna da qual as informações são recuperadas.

*szColumnName*

O nome da coluna para a qual as informações são buscadas.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer é dependente de *InfoLevel*. O chamador deve ser configurado para alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer que é passado em *pvResult*.

*InfoLevel*

O tipo de informações a serem recuperadas para a coluna especificada por *szColumnName*. O formato dos dados armazenados em *pvResult* depende desse parâmetro. Para o esquema da tabela temporária, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

Esses *InfoLevels* são diferenciados por:

  - JET_ColInfoListSortColumnid classificará a tabela temporária por *columnid*.

  - JET_ColInfoListCompact compactará a saída. Para obter mais informações sobre a saída compacta, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

As opções a seguir estão disponíveis para uso com esse parâmetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações. <em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Isso é semelhante a uma estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Se essa função falhar, a estrutura conterá dados indefinidos.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Assim como JET_ColInfo, <em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e identificada pelo membro <strong>TableName</strong> da estrutura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se essa função falhar, a estrutura conterá dados indefinidos.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>O mesmo que JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>O mesmo que JET_ColInfoList; no entanto, a tabela resultante é classificada por columnid, em vez de nome da coluna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor for preterido e o uso dele retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Assim como JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> esse valor é introduzido no Windows Vista.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Retornar apenas colunas não derivadas (se a tabela for derivada de um modelo).</p><p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> esse valor é introduzido Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Retorna apenas o nome da coluna e columnid de cada coluna.</p><p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> esse valor é introduzido no Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Classifique a lista de colunas retornada por ColumnID (o padrão é classificar a lista por nome de coluna).</p><p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> esse valor é introduzido no Windows Vista.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errColumnNotFound</p> | <p>A coluna denominada <em>szColumnName</em> não foi encontrada na tabela.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Um <em>InfoLevel</em> inadequado foi especificado.</p> | 
| <p>JET_errInvalidName</p> | <p>Esse erro pode ser retornado se:</p><ul><li><p>Um nome inadequado para <em>szTableName</em> foi fornecido.</p></li><li><p>Um nome inadequado para <em>szColumnName</em> foi fornecido.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Esse erro pode ser retornado se:</p><ul><li><p>Um <em>InfoLevel</em> inadequado foi especificado.</p></li><li><p>Um <em>SZTABLENAME</em> nulo foi passado.</p></li><li><p>O buffer é muito pequeno.</p></li></ul> | 



#### <a name="remarks"></a>Comentários

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) e **JetGetColumnInfo** recuperam informações sobre uma coluna. A diferença entre eles é como a tabela é identificada:

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica uma tabela por *TableName*.

  - **JetGetColumnInfo** identifica uma tabela pela combinação de *DBID* e *szTableName* .

Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta. A tabela temporária contém dados e a estrutura de [JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para atravessar a tabela temporária. A tabela temporária deve ser fechada com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetColumnInfoW</strong> (Unicode) e <strong>JetGetColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros de mecanismo Armazenamento extensível](./extensible-storage-engine-errors.md)  
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
