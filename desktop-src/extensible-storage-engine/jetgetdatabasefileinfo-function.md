---
description: 'Saiba mais sobre: função JetGetDatabaseFileInfo'
title: Função JetGetDatabaseFileInfo
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b19d783480a8d82485bce32689b8d49e046b0285
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623502"
---
# <a name="jetgetdatabasefileinfo-function"></a>Função JetGetDatabaseFileInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetdatabasefileinfo-function"></a>Função JetGetDatabaseFileInfo

A função **JetGetDatabaseFileInfo** recupera vários tipos de informações sobre o banco de dados. Essa API pode ser chamada enquanto um banco de dados estiver anexado ou online (com [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ou enquanto o banco de dados ou o mecanismo de banco de dados estiver offline (com **JetGetDatabaseFileInfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*szDatabaseName*

O caminho do banco de dados do qual recuperar as informações.

*pvResult*

Ponteiro para um buffer que receberá as informações especificadas. O tamanho do buffer, em bytes, é passado em *cbMax*.

Se essa função falhar, o conteúdo de *pvResult* será indefinido.

As informações armazenadas no *pvResult* dependem do *InfoLevel*.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult*.

*InfoLevel*

*InfoLevel* especifica que tipo de informações devem ser recuperadas sobre o banco de dados especificado. Ele afeta como o *pvResult* é interpretado. Alguns objetos *InfoLevel* estão disponíveis somente na versão offline (**JetGetDatabaseFileInfo**) ou online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) da API.

Se o buffer *pvResult* fornecido for muito pequeno, JET_errInvalidBufferSize ou JET_errBufferTooSmall serão retornados, dependendo do *InfoLevel*.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> será interpretado como um QWORD (8 bytes). Retorna o tamanho do banco de dados em bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> será interpretado como um <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. A estrutura de <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> será preenchida com informações referentes ao banco de dados especificado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> será interpretado como um <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. A estrutura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> será preenchida com informações referentes ao banco de dados especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> será interpretado como um bool (4 bytes). Isso retornará se o mecanismo de banco de dados tem, no momento, qualquer banco de dados aberto ou anexado.</p>
<p><strong>Windows XP:</strong> esse valor é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> será interpretado como um longo não assinado. Isso retornará o tamanho da página do banco de dados em bytes.</p>
<p><strong>Windows XP:</strong> esse valor é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Esses <em>InfoLevels</em> ainda não têm suporte e retornam valores padrão. Não use esses <em>InfoLevels</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Esses <em>InfoLevels</em> ainda não têm suporte e retornam valores padrão. Não use esses <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>O mesmo que JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento. Não use esses <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>O mesmo que JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:</strong> esse valor de <em>InfoLevel</em> é introduzido no Windows Vista.</p>
<p><em>pvResult</em> será tratado como um ponteiro para um DWORD. Retorna um valor de enumeração, indicando que tipo de arquivo o mecanismo considera isso. Os tipos de arquivo são listados na tabela a seguir. para obter mais informações sobre esses tipos de arquivos e seu uso para o mecanismo, consulte <a href="gg294069(v=exchg.10).md">arquivos do mecanismo de Armazenamento extensível</a>.</p>
<div class="tableSection">
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_filetypeUnknown</p></td>
<td><p>O tipo de arquivo é desconhecido ou não é um tipo de arquivo ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>O arquivo é um arquivo de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>O arquivo é um arquivo de log de transações.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>O arquivo é um arquivo de ponto de verificação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>O arquivo é um arquivo de banco de dados temporário.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col  />
<col  />
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>O <em>InfoLevel</em> solicitado foi JET_DbInfoIsam. Isso não tem suporte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>O buffer fornecido em <em>cbMax</em> é muito pequeno para as informações desejadas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>O buffer fornecido em <em>cbMax</em> não é o tamanho correto para as informações desejadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Esse erro será retornado por <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando a DBID fornecida não for um banco de dados válido (anexado). Esse erro será retornado por <strong>JetGetDatabaseFileInfo</strong> e <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando um <em>InfoLevel</em> solicitado não for suportado por essa versão da função.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, os dados solicitados serão retornados no buffer de saída.

Se essa função falhar, o buffer de saída estará em um estado indefinido.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p></td>
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
<td><p>Implementado como <strong>JetGetDatabaseFileInfoW</strong> (Unicode) e <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
