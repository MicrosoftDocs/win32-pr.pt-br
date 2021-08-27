---
description: 'Saiba mais sobre: Função JetGetObjectInfo'
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
ms.openlocfilehash: 824c19fbb1fb1e479b805eb45bf8ff56458110d0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469783"
---
# <a name="jetgetobjectinfo-function"></a>Função JetGetObjectInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetobjectinfo-function"></a>Função JetGetObjectInfo

A **função JetGetObjectInfo** recupera informações sobre objetos de banco de dados. Atualmente, há suporte apenas para tabelas. [JetGetTableInfo](./jetgettableinfo-function.md) pode ser usado para buscar mais informações do que **JetGetObjectInfo**.

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

O contexto de sessão do banco de dados a ser usado.

*Dbid*

O banco de dados do qual as informações são recuperadas.

*objtyp*

Os objetos que contêm informações a serem recuperadas. Atualmente, apenas JET_objtypNil e JET_objtypTable têm suporte, ambos se comportam de forma idêntica. Somente tabelas serão recuperadas.

*szContainerName*

Esse parâmetro é reservado para uso futuro e passa **NULL.** O nome dos tipos de objetos sobre os quais recuperar informações.

*szObjectName*

O nome do objeto que contém informações a recuperar. Quando *InfoLevel* usa as JET_ObjInfoList ou JET_ObjInfoListNoStats para recuperar uma lista de todos os objetos, esse valor deve ser **NULL** ou uma cadeia de caracteres vazia.

No momento, há suporte apenas para nomes de tabela.

*pvResult*

Ponteiro para um buffer que recebe as informações especificadas.

O tamanho do buffer, em bytes, é passado em *cbMax.* Em caso de falha, o *conteúdo de pvResult* é indefinido.

As informações armazenadas em *pvResult dependem* de *InfoLevel.*

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult.*

*InfoLevel*

Especifica qual tipo de informação recuperar para o objeto especificado. Ela afeta como *pvResult* é interpretado.

As opções a seguir estão disponíveis para definir para esse parâmetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult</em> é interpretado como uma <a href="gg269353(v=exchg.10).md">estrutura JET_OBJECTINFO</a> dados.</p><p>A <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> é preenchida com informações referentes ao objeto chamado <em>em szObjectName</em>.</p><p>Se o chamador não quiser saber o número de registros e páginas para o objeto, considere usar JET_ObjInfoNoStats nível de informações, o que pode ser mais rápido, pois as estatísticas não estão incluídas.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult</em> é interpretado como uma estrutura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> dados. Informações sobre todos os objetos são recuperadas. Uma tabela temporária será criada e as informações necessárias para percorrer a tabela temporária são descritas na <a href="gg269348(v=exchg.10).md">estrutura JET_OBJECTLIST</a> dados. Para obter mais informações, <a href="gg269348(v=exchg.10).md">consulte JET_OBJECTLIST</a>. Se o chamador não quiser saber o número de registros e páginas para o objeto, considere usar JET_ObjInfoListNoStats, o que pode ser mais rápido.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>Preterido e sem suporte no momento.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult</em> é interpretado como uma estrutura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> dados. Informações sobre todos os objetos são recuperadas. Uma tabela temporária será criada e as informações necessárias para percorrer a tabela temporária são descritas na <a href="gg269348(v=exchg.10).md">estrutura JET_OBJECTLIST</a> dados. Para obter mais informações, <a href="gg269348(v=exchg.10).md">consulte JET_OBJECTLIST</a>. JET_ObjInfoListNoStats é idêntico ao JET_ObjInfoList, exceto que as colunas que relatam o número de registros (<em>columnidcRecord</em>) e pages (<em>columnidcPage</em>) não serão atualizadas.</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. O tamanho máximo do objeto está em páginas. No momento, somente as tabelas serão retornadas.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult</em> é interpretado como um <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Informações sobre apenas o objeto determinado <em>em szObjectName</em> serão recuperadas.</p><p>A <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> de dados será preenchida com informações referentes ao objeto chamado <em>em szObjectName</em>.</p><p>JET_ObjInfoNoStats é idêntico ao JET_ObjInfo, exceto que os campos que relatam o número de registros e páginas são definidos como zero.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>Preterido e sem suporte no momento.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>Preterido e sem suporte no momento.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>Preterido e sem suporte no momento.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O tamanho do buffer determinado em <em>cbMax</em> era muito pequeno para manter as informações desejadas.</p> | 
| <p>JET_errInvalidName</p> | <p>Um nome inválido foi dado <em>em szObjectName</em> ou <em>szContainerName</em>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro ruim foi dado. É possível que um nível ruim foi passado para <em>InfoLevel.</em></p> | 



#### <a name="remarks"></a>Comentários

Se **JetGetObjectInfo** criar com êxito uma tabela temporária (por exemplo, JET_ObjInfoList ou JET_ObjInfoNoStats), o chamador será responsável por fechar a tabela temporária com [JetCloseTable](./jetclosetable-function.md).

**Atualmente, JetGetObjectInfo** dá suporte apenas à recuperação de informações sobre tabelas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</p> | 



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
