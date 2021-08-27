---
description: 'Saiba mais sobre: Função JetGetTableInfo'
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
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465793"
---
# <a name="jetgettableinfo-function"></a>Função JetGetTableInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgettableinfo-function"></a>Função JetGetTableInfo

A **função JetGetTableInfo** recupera várias informações sobre uma tabela em um banco de dados.

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

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

A tabela à que as informações se aplica.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer depende de *InfoLevel.* É responsabilidade do chamador alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult.*

*InfoLevel*

O tipo de informações que serão recuperadas para a tabela especificada por *tableid*. O formato dos dados armazenados em *pvResult* depende de *InfoLevel.*

As seguintes opções podem ser definidas para esse parâmetro:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>pvResult</em> é interpretado como uma <a href="gg269353(v=exchg.10).md">estrutura JET_OBJECTINFO</a> dados. Se o método for bem-sucedido, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estrutura de dados será preenchida com os dados apropriados. Se falhar, o conteúdo será indefinido.</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>pvResult</em> é tratado como uma matriz de dois <a href="gg269248(v=exchg.10).md">JET_DBID</a> objetos. O identificador de banco de dados do banco de dados que possui a tabela é armazenado nessa matriz duas vezes.</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable foi preterido. A API retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName recupera o nome da tabela e a armazena em <em>pvResult</em>. Se o buffer for muito pequeno, o comportamento será indefinido.</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany recupera o nome da tabela e o armazena em <em>pvResult</em>. Se o buffer for muito pequeno, o comportamento será indefinido.</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC foi preterido. A API retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt foi preterido. A API retornará JET_errQueryNotSupported.</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC foi preterido. A API retornará JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>pvResult</em> é interpretado como uma matriz de dois ULONGs:</p><ul><li><p>O primeiro <strong>ULONG</strong> é o número de páginas na tabela.</p></li><li><p>O segundo <strong>ULONG</strong> é a densidade de destino das páginas da tabela.</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>pvResult</em> é interpretado como <strong>um ULONG.</strong> O <strong>ULONG</strong> é a soma do número de páginas que estão disponíveis na tabela, seus índices e a árvore de valor longo.</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>pvResult</em> é interpretado como <strong>um ULONG.</strong> O <strong>ULONG</strong> é a soma do número de páginas pertencentes à tabela (incluindo seus índices, a árvore de valor longo e todas as páginas disponíveis).</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>O comportamento da API depende do tamanho do buffer passado para a API. Dois <em>valores cbMax</em> devem ser pelo menos ( 2 * sizeof( ULONG ) ).</p><ul><li><p>Se <em>cbMax</em> for ( 2 * sizeof( ULONG ), <em>pvResult</em> será interpretado como uma matriz de dois ULONGs:</p><ul><li><p>O primeiro <strong>ULONG</strong> é o número de Extensão De Propriedade da tabela.</p></li><li><p>O segundo <strong>ULONG</strong> é o número de Extensão Disponíveis da tabela.</p></li></ul></li><li><p><em>pvResult</em> é interpretado como uma matriz de:</p><ul><li><p>O primeiro <strong>ULONG</strong> é o número de Extensão De Propriedade da tabela.</p></li><li><p>O segundo <strong>ULONG</strong> é o número de Extensão Disponíveis da tabela.</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>pvResult é interpretado</em> como um buffer de cadeia de caracteres. O buffer deve ser pelo menos JET_cbNameMost + 1, incluindo o NULL de <strong>terminação.</strong> Se a tabela for uma tabela derivada, o buffer será preenchido com o nome da tabela da qual a tabela derivada herdou sua DDL. Se a tabela não for uma tabela derivada, o buffer será uma cadeia de caracteres vazia.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O buffer era muito pequeno.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Um <em>InfoLevel</em> preterido foi especificado.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>O buffer não era o tamanho certo.</p> | 
| <p>JET_errInvalidOperation</p> | <p>A tabela passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</p> | 
| <p>JET_errObjectNotFound</p> | <p>A tabela passada era uma tabela temporária e o <em>InfoLevel</em> solicitado não pode ser recuperado para uma tabela temporária.</p> | 
| <p>JET_errQueryNotSupported</p> | <p>Não <em>há suporte para o InfoLevel.</em></p> | 
| <p>JET_errTableInUse</p> | <p>A tabela está sendo usada por outra operação de banco de dados.</p> | 
| <p>JET_errTableLocked</p> | <p>A tabela é bloqueada por outra operação de banco de dados.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>A tabela está sendo usada pelo sistema. Esse aviso é nãofatal.</p> | 



#### <a name="remarks"></a>Comentários

Algumas informações não são válidas para tabelas temporárias (consulte [JetOpenTempTable](./jetopentemptable-function.md)).

As estatísticas de tabela incluem o número de registros e o número de páginas no índice clusterizado (ou seja, o índice que contém os dados de registro). As estatísticas de índice são acessadas separadamente por nome, usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</p> | 



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
