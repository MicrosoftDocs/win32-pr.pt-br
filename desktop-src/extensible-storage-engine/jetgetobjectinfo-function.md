---
description: 'Saiba mais sobre: função JetGetObjectInfo'
title: Função JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798095"
---
# <a name="jetgetobjectinfo-function"></a>Função JetGetObjectInfo


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>Função JetGetObjectInfo

A função **JetGetObjectInfo** recupera informações sobre objetos de banco de dados. Atualmente, há suporte apenas para tabelas. [JetGetTableInfo](./jetgettableinfo-function.md) pode ser usado para buscar mais informações do que **JetGetObjectInfo**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado.

*DBID*

O banco de dados do qual as informações são recuperadas.

*objtyp*

Os objetos que contêm informações a serem recuperadas. Atualmente, há suporte apenas para JET_objtypNil e JET_objtypTable, os quais se comportam de forma idêntica. Somente tabelas serão recuperadas.

*szContainerName*

Esse parâmetro é reservado para uso futuro e passa **nulo**. O nome dos tipos de objetos sobre os quais recuperar informações.

*szObjectName*

O nome do objeto que contém informações a serem recuperadas. Quando *InfoLevel* usa as opções JET_ObjInfoList ou JET_ObjInfoListNoStats para recuperar uma lista de todos os objetos, esse valor deve ser **nulo** ou uma cadeia de caracteres vazia.

Somente os nomes de tabela têm suporte no momento.

*pvResult*

Ponteiro para um buffer que recebe as informações especificadas.

O tamanho do buffer, em bytes, é passado em *cbMax*. Em caso de falha, o conteúdo de *pvResult* é indefinido.

As informações armazenadas no *pvResult* dependem do *InfoLevel*.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult*.

*InfoLevel*

Especifica o tipo de informações a serem recuperadas para o objeto especificado. Ele afeta como o *pvResult* é interpretado.

As opções a seguir estão disponíveis para serem definidas para esse parâmetro.

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
<td><p>JET_ObjInfo</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p>
<p>A estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> é preenchida com informações referentes ao objeto nomeado em <em>szObjectName</em>.</p>
<p>Se o chamador não quiser saber o número de registros e páginas do objeto, considere usar JET_ObjInfoNoStats nível de informações, o que pode ser mais rápido, pois as estatísticas não são incluídas.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoList</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . As informações sobre todos os objetos são recuperadas. Uma tabela temporária será criada e as informações necessárias para atravessar a tabela temporária serão descritas na estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Para obter mais informações, consulte <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Se o chamador não quiser saber o número de registros e páginas do objeto, considere o uso de JET_ObjInfoListNoStats, que pode ser mais rápido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoListACM</p></td>
<td><p>Preterido e não tem suporte no momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoListNoStats</p></td>
<td><p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . As informações sobre todos os objetos são recuperadas. Uma tabela temporária será criada e as informações necessárias para atravessar a tabela temporária serão descritas na estrutura de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Para obter mais informações, consulte <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats é idêntico a JET_ObjInfoList, exceto que as colunas que relatam o número de registros (<em>columnidcRecord</em>) e as páginas (<em>columnidcPage</em>) não serão atualizadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoMax</p></td>
<td><p><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. O tamanho máximo do objeto está em páginas. No momento, apenas tabelas serão retornadas.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoNoStats</p></td>
<td><p><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Informações sobre apenas o objeto fornecido em <em>szObjectName</em> serão recuperadas.</p>
<p>A estrutura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> será preenchida com informações referentes ao objeto nomeado em <em>szObjectName</em>.</p>
<p>JET_ObjInfoNoStats é idêntico a JET_ObjInfo, exceto que os campos que relatam o número de registros e páginas são definidos como zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoRulesLoaded</p></td>
<td><p>Preterido e não tem suporte no momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoSysTabCursor</p></td>
<td><p>Preterido e não tem suporte no momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoSysTabReadOnly</p></td>
<td><p>Preterido e não tem suporte no momento.</p></td>
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
<td><p>O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno para conter as informações desejadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Um nome inválido foi fornecido em <em>szObjectName</em> ou <em>szContainerName</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inadequado foi fornecido. É possível que um nível inadequado seja passado para <em>InfoLevel</em>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se **JetGetObjectInfo** criar com êxito uma tabela temporária (por exemplo, JET_ObjInfoList ou JET_ObjInfoNoStats), o chamador será responsável por fechar a tabela temporária com [JetCloseTable](./jetclosetable-function.md).

Atualmente, o **JetGetObjectInfo** dá suporte apenas à recuperação de informações sobre tabelas.

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
<td><p>Implementado como <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
