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
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104173227"
---
# <a name="jetgettablecolumninfo-function"></a>Função JetGetTableColumnInfo


_**Aplica-se a:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ColInfo</p></td>
<td><p><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e os campos da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> são preenchidos adequadamente. JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Isso é semelhante a uma estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Se essa função falhar, a estrutura conterá dados indefinidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>pvResult</em> é interpretado como um <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo e JET_ColInfoByColid recuperam as mesmas informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se essa função falhar, a estrutura conterá dados indefinidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se essa função for realizada com sucesso, a estrutura será populada com os valores apropriados. Uma tabela temporária é aberta e identificada pelo membro <em>TableName</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. A tabela deve ser fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se essa função falhar, a estrutura conterá dados indefinidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>O mesmo que JET_ColInfoList, no entanto, a tabela resultante é classificada por <em>columnid</em>, em vez do nome da coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor for preterido e o uso dele retornará JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>O mesmo que JET_ColInfoBase, <em>pvResult</em> é interpretado como um <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, exceto que esse <em>InfoLevel</em> indica que a coluna solicitada (<em>szColumName</em>) não é o nome da coluna de cadeia de caracteres, mas um ponteiro para um <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista:  </strong> Isso está disponível no Windows Vista e versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Retornar apenas colunas não derivadas (se a tabela for derivada de um modelo).</p>
<p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Retorna apenas o nome da coluna e columnid de cada coluna.</p>
<p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Classifique a lista de colunas retornada por ColumnID (o padrão é classificar a lista por nome de coluna).</p>
<p>Esse valor pode ser logicamente ou inserido no <em>InfoLevel</em>, quando o <em>InfoLevel</em> de base é JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Esse valor é introduzido no Windows Vista.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna denominada <em>szColumnName</em> não foi encontrada na tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Um <em>InfoLevel</em> inadequado foi especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Esse erro pode ser retornado se:</p>
<ul>
<li><p>Um nome inadequado para <em>szTableName</em> foi fornecido.</p></li>
<li><p>Um nome inadequado para <em>szColumnName</em> foi fornecido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Esse erro pode ser retornado se:</p>
<ul>
<li><p>Um <em>InfoLevel</em> inadequado foi especificado.</p></li>
<li><p>Um <em>SZTABLENAME</em> nulo foi passado.</p></li>
<li><p>O buffer é muito pequeno.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

**JetGetTableColumnInfo** e [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperam informações sobre uma coluna. A diferença entre eles é como a tabela é identificada:

  - **JetGetTableColumnInfo** identifica uma tabela por *TableName*.

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica uma tabela pela combinação de *DBID* e *szTableName* .

Ao recuperar dados com JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, uma tabela temporária será aberta. A tabela temporária contém dados e a estrutura de [JET_COLUMNLIST](./jet-columnlist-structure.md) contém informações suficientes para atravessar a tabela temporária. A tabela temporária deve ser fechada com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetGetTableColumnInfoW</strong> (Unicode) e <strong>JetGetTableColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
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
