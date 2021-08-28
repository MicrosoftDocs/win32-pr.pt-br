---
description: 'Saiba mais sobre: função JetGetTableColumnInfo'
title: Função JetGetTableColumnInfo
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925ade657a4184d5b1cac447aa43619f375bc0b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468953"
---
# <a name="jetgettablecolumninfo-function"></a>Função JetGetTableColumnInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgettablecolumninfo-function"></a>Função JetGetTableColumnInfo

A função **JetGetTableColumnInfo** recupera informações sobre uma coluna de tabela.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela que contém a coluna para a qual obter informações.

*szColumnName*

O nome da coluna para a qual obter informações.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer é dependente de *InfoLevel*. O chamador deve ser configurado para alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer que foi passado em *pvResult*.

*InfoLevel*

O tipo de informações que serão recuperadas para a coluna especificada por *szColumnName*. O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*. Para o esquema da tabela temporária, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid classificará a tabela temporária por *columnid*.

  - JET_ColInfoListCompact compactará a saída. Para obter mais informações sobre a saída compacta, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

As seguintes opções podem ser definidas para este parâmetro:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente. JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Isso é semelhante a uma estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Se essa função falhar, a estrutura conterá dados indefinidos.</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se essa função falhar, a estrutura conterá dados indefinidos.</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se essa função falhar, a estrutura conterá dados indefinidos.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>O mesmo que JET_ColInfoList, no entanto, a tabela resultante é classificada por <em>columnid</em>, em vez do nome da coluna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor for preterido e o uso dele retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>O mesmo que JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> isso está disponível no Windows Vista e versões posteriores.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Retornar apenas colunas não derivadas (se a tabela for derivada de um modelo).</p><p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p><p><strong>Windows Vista:</strong> esse valor é introduzido no Windows Vista.</p> | 
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

**JetGetTableColumnInfo** e [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperam informações sobre uma coluna. A diferença entre eles é como a tabela é identificada:

  - **JetGetTableColumnInfo** identifica uma tabela por *TableName*.

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica uma tabela pela combinação de *DBID* e *szTableName* .

Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta. A tabela temporária contém dados e a estrutura de [JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para atravessar a tabela temporária. A tabela temporária deve ser fechada com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetTableColumnInfoW</strong> (Unicode) e <strong>JetGetTableColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md)  
[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
