---
description: 'Saiba mais sobre: função JetGetTableInfo'
title: Função JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922661"
---
# <a name="jetgettableinfo-function"></a>Função JetGetTableInfo


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>Função JetGetTableInfo

A função **JetGetTableInfo** recupera várias partes de informações sobre uma tabela em um banco de dados.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela à qual as informações se aplicam.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer é dependente de *InfoLevel*. É responsabilidade do chamador alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer que foi passado em *pvResult*.

*InfoLevel*

O tipo de informações que serão recuperadas para a tabela especificada por *TableName*. O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.

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
<td><p>JET_TblInfo</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Se o método tiver sucesso, a estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> será preenchida com os dados apropriados. Se falhar, o conteúdo será indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>pvResult</em> é tratado como uma matriz de dois objetos <a href="gg269248(v=exchg.10).md">JET_DBID</a> . O identificador de banco de dados do banco de dados que possui a tabela é armazenado nessa matriz duas vezes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable é preterida. A API retornará JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName recupera o nome da tabela e a armazena em <em>pvResult</em>. Se o buffer for muito pequeno, o comportamento será indefinido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany recupera o nome da tabela e a armazena em <em>pvResult</em>. Se o buffer for muito pequeno, o comportamento será indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC é preterida. A API retornará JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt é preterida. A API retornará JET_errQueryNotSupported.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC é preterida. A API retornará JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> é interpretado como uma matriz de dois ULONGs:</p>
<ul>
<li><p>O primeiro <strong>ULONG</strong> é o número de páginas na tabela.</p></li>
<li><p>O segundo <strong>ULONG</strong> é a densidade de destino das páginas da tabela.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> é interpretado como um <strong>ULONG</strong>. O <strong>ULONG</strong> é a soma do número de páginas que estão disponíveis na tabela, seus índices e a árvore de valor longo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> é interpretado como um <strong>ULONG</strong>. O <strong>ULONG</strong> é a soma do número de páginas pertencentes à tabela (incluindo seus índices e a árvore de valor longo e todas as páginas disponíveis aqui).</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>O comportamento da API depende do tamanho do buffer que é passado para a API. Dois valores de <em>cbMax</em> devem ser pelo menos (2 * sizeof (ULong)).</p>
<ul>
<li><p>Se <em>cbMax</em> for (2 * sizeof (ULong)), <em>pvResult</em> será interpretado como uma matriz de dois ULONGs:</p>
<ul>
<li><p>O primeiro <strong>ULONG</strong> é o número de extensões de propriedade da tabela.</p></li>
<li><p>O segundo <strong>ULONG</strong> é o número de extensões disponíveis da tabela.</p></li>
</ul></li>
<li><p><em>pvResult</em> é interpretado como uma matriz de:</p>
<ul>
<li><p>O primeiro <strong>ULONG</strong> é o número de extensões de propriedade da tabela.</p></li>
<li><p>O segundo <strong>ULONG</strong> é o número de extensões disponíveis da tabela.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>pvResult</em> é interpretado como um buffer de cadeia de caracteres. O buffer deve ser pelo menos JET_cbNameMost + 1, incluindo o <strong>nulo</strong>de terminação. Se a tabela for uma tabela derivada, o buffer será preenchido com o nome da tabela da qual a tabela derivada herdou sua DDL. Se a tabela não for uma tabela derivada, o buffer será uma cadeia de caracteres vazia.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>O buffer era muito pequeno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Foi especificado um <em>InfoLevel</em> preterido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>O buffer não era o tamanho correto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>A tabela que foi passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>A tabela que foi passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p>Não há suporte para o <em>InfoLevel</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>A tabela está sendo usada por outra operação de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>A tabela está bloqueada por outra operação de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>A tabela está sendo usada pelo sistema. Este aviso é não fatal.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Algumas informações não são válidas para tabelas temporárias (consulte [JetOpenTempTable](./jetopentemptable-function.md)).

As estatísticas de tabela incluem o número de registros e o número de páginas no índice clusterizado (ou seja, o índice que contém os dados de registro). As estatísticas de índice são acessadas separadamente por nome, usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

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
<td><p>Implementado como <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
