---
description: 'Saiba mais sobre: função JetGetIndexInfo'
title: Função JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748858"
---
# <a name="jetgetindexinfo-function"></a>Função JetGetIndexInfo


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>Função JetGetIndexInfo

A função **JetGetIndexInfo** recupera informações sobre um índice.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O identificador de banco de dados a ser usado para a chamada à API.

*szTableName*

O nome da tabela que contém o índice com as informações a serem recuperadas.

*szIndexName*

O nome do índice com as informações a serem recuperadas.

*pvResult*

Ponteiro para um buffer que receberá as informações desejadas. O buffer deve ser alinhado para conter o tipo necessário. O tipo do buffer é dependente do parâmetro *InfoLevel* .

*cbResult*

O tamanho, em bytes, do buffer passado como *pvResult*.

*InfoLevel*

As informações que serão armazenadas em *pvResult*. As opções a seguir podem ser usadas para esse parâmetro.

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvResult</em> é interpretado como um ULONG. Em caso de sucesso, o ULONG mantém a contagem de índices na tabela especificada. <em>szIndexName</em> é ignorado. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvResult</em> é interpretado como um <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Em caso de sucesso, a estrutura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid é preterida. Use JET_IdxInfoLCID e a macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> em vez disso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvResult</em> é interpretado como um LCID. Em caso de sucesso, o LCID mantém o identificador de localidade do índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p>
<p><strong>Windows XP:  </strong> O JET_IdxInfoLCID é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC está obsoleta.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC está obsoleta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> é interpretado como um ULONG. Em caso de sucesso, o ULONG mantém o uso do espaço do índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor está obsoleta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvResult</em> é interpretado como um ushort. Em caso de sucesso, o USHORT mantém o valor de <em>cbVarSegMac</em> usado quando o índice foi criado. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbVarSegMac</em>. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvResult</em> é interpretado como um ushort. Em caso de sucesso, o USHORT mantém o valor de <em>cbKeyMost</em> usado quando o índice foi criado. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbKeyMost</em>. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p>
<p><strong>Windows Vista:  </strong> O JET_IdxInfoKeyMost é introduzido no Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex é introduzido no Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 é introduzido no Windows 7.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>O índice especificado não pode ser encontrado na tabela especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>O buffer passado como <em>pvResult</em> era muito pequeno. O conteúdo do buffer está indefinido.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

**JetGetIndexInfo** e [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperam informações idênticas sobre um índice. A diferença está em como a tabela é especificada. **JetGetIndexInfo** espera um banco de dados (*DBID*) e o nome de uma tabela (*szTableName*), enquanto [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera um identificador de tabela (*TableName*).

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
<td><p>Implementado como <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
