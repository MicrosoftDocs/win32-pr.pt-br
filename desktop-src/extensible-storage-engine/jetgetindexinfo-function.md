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
ms.openlocfilehash: e4d7c835d5077d2bfee87025b202480a888de981
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988579"
---
# <a name="jetgetindexinfo-function"></a>Função JetGetIndexInfo


_**Aplica-se a:** Windows | Windows Servidor_

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> é interpretado como um ULONG. Em caso de sucesso, o ULONG mantém a contagem de índices na tabela especificada. <em>szIndexName</em> é ignorado. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> é interpretado como um <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Em caso de sucesso, a estrutura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid é preterida. Use JET_IdxInfoLCID e a macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> em vez disso.</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> é interpretado como um LCID. Em caso de sucesso, o LCID mantém o identificador de localidade do índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p><p><strong>Windows XP:</strong> o JET_IdxInfoLCID é introduzido no Windows XP.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Em caso de sucesso, a estrutura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recebe informações sobre o índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC está obsoleta.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC está obsoleta.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> é interpretado como um ULONG. Em caso de sucesso, o ULONG mantém o uso do espaço do índice. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor está obsoleta.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> é interpretado como um ushort. Em caso de sucesso, o USHORT mantém o valor de <em>cbVarSegMac</em> usado quando o índice foi criado. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbVarSegMac</em>. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> é interpretado como um ushort. Em caso de sucesso, o USHORT mantém o valor de <em>cbKeyMost</em> usado quando o índice foi criado. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma descrição de <em>cbKeyMost</em>. Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p><p><strong>Windows Vista:</strong> o JET_IdxInfoKeyMost é introduzido no Windows Vista.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex é introduzido no Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult</em> é interpretado como uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Em caso de falha, o conteúdo de <em>pvBuffer</em> é indefinido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 é introduzido no Windows 7.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errIndexNotFound</p> | <p>O índice especificado não pode ser encontrado na tabela especificada.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>O buffer passado como <em>pvResult</em> era muito pequeno. O conteúdo do buffer está indefinido.</p> | 



#### <a name="remarks"></a>Comentários

**JetGetIndexInfo** e [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperam informações idênticas sobre um índice. A diferença está em como a tabela é especificada. **JetGetIndexInfo** espera um banco de dados (*DBID*) e o nome de uma tabela (*szTableName*), enquanto [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera um identificador de tabela (*TableName*).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
