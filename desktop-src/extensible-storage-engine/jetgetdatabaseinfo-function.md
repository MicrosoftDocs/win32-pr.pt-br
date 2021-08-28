---
description: 'Saiba mais sobre: função JetGetDatabaseInfo'
title: Função JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 335ad13411dbfcc83dce559eb4b77adefcc8a5da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477952"
---
# <a name="jetgetdatabaseinfo-function"></a>Função JetGetDatabaseInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetdatabaseinfo-function"></a>Função JetGetDatabaseInfo

A função **JetGetDatabaseInfo** recupera vários tipos de informações sobre o banco de dados. Essa API pode ser chamada enquanto um banco de dados estiver anexado ou online (com **JetGetDatabaseInfo**) ou enquanto o banco de dados ou o mecanismo de banco de dados estiver offline (com [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*DBID*

O [JET_DBID](./jet-dbid.md) do banco de dados do qual recuperar as informações.

*pvResult*

Ponteiro para um buffer que receberá as informações especificadas. O tamanho do buffer, em bytes, é passado em *cbMax*.

Em caso de falha, o conteúdo de *pvResult* é indefinido.

As informações armazenadas no *pvResult* dependem do *InfoLevel*.

*cbMax*

O tamanho, em bytes, do buffer que foi passado em *pvResult*.

*InfoLevel*

*InfoLevel* especifica que tipo de informações devem ser recuperadas sobre o banco de dados especificado. Ele afeta como o *pvResult* é interpretado. Alguns *InfoLevel* estão disponíveis somente na versão offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) ou online (**JetGetDatabaseInfo**) da API.

Se o buffer *pvResult* fornecido for muito pequeno, JET_errInvalidBufferSize ou JET_errBufferTooSmall serão retornados, dependendo do *InfoLevel*.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>Ainda não tem suporte e retorna valores padrão. Não use.</p> | 
| <p>JET_DbInfoConnect</p> | <p>Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento. Não use.</p> | 
| <p>JET_DbInfoCountry</p> | <p>Ainda não tem suporte e retorna valores padrão. Não use.</p> | 
| <p>JET_DbInfoCp</p> | <p>Ainda não tem suporte e retorna valores padrão. Não use.</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> será interpretado como um buffer de cadeia de caracteres (Char *). Um buffer de MAX_PATH é sugerido, porém não obrigatório. Se o buffer não for longo o suficiente, JET_errBufferTooSmall será retornado. A cadeia de caracteres será populada com o caminho do banco de dados para esta DBID.</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> será interpretado como um DWORD (4 bytes). Retorna o tamanho do banco de dados em páginas.</p> | 
| <p>JET_DbInfoIsam</p> | <p>Esses <em>InfoLevels</em> foram preteridos e não têm suporte no momento. Não use.</p> | 
| <p>JET_DbInfoLCID</p> | <p>(Windows XP e posterior) este <em>InfoLevel</em> foi originalmente especificado como: JET_DbInfoLangid (Windows 2000)</p><p><em>pvResult</em> será interpretado como um longo. Isso retorna o LCID (identificador de localidade) associado a este banco de dados.</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> será interpretado como um <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. A estrutura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> será preenchida com informações relacionadas ao banco de dados especificado.</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> será interpretado como um <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Isso retorna se o banco de dados está aberto em modo exclusivo. Se o banco de dados estiver em modo exclusivo JET_bitDbExclusive será definido no <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fornecido, caso contrário, zero será definido. Observe que outras opções de <em>grbit</em> de banco de dados para <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> e <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> não são retornadas.</p> | 
| <p>JET_DbInfoPageSize</p> | <p>disponível somente no Windows XP e versões posteriores. <em>pvResult</em> será interpretado como um longo não assinado. Isso retornará o tamanho da página do banco de dados em bytes.</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> será interpretado como um DWORD. Isso retorna o espaço disponível para o banco de dados em páginas.</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> será interpretado como um DWORD. Isso retorna o espaço de Propriedade do banco de dados em páginas.</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> será interpretado como um longo. Isso retornará um maior que o nível máximo para o qual as transações podem ser aninhadas. Se <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for chamado (em um modo de aninhamento, ou seja, na mesma sessão, sem uma confirmação ou reversão) quantas vezes esse valor, na última chamada JET_errTransTooDeep será retornado de <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>. observe o valor em Windows 2000, Windows XP e Windows Server 2003 é 7.</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> será interpretado como um longo. Isso retorna a versão principal nativa do mecanismo de banco de dados. esse valor é 0x620 para Windows 2000, Windows XP e Windows Server 2003.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno (ou não está correto) para manter as informações desejadas.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>O <em>InfoLevel</em> solicitado foi JET_DbInfoIsam. Isso não tem suporte.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>O tamanho do buffer fornecido em <em>cbMax</em> era muito pequeno (ou não está correto) para manter as informações desejadas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <strong>JetGetDatabaseInfo</strong> quando o <a href="gg269248(v=exchg.10).md">JET_DBID</a> fornecido não for um banco de dados (anexado) válido. Esse erro será retornado por <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> e <strong>JetGetDatabaseInfo</strong> quando um <em>InfoLevel</em> solicitado não for suportado por essa versão da função.</p> | 



Em caso de sucesso, os dados solicitados serão retornados no buffer de saída.

Em caso de falha, o buffer de saída estará em um estado indefinido.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetDatabaseInfoW</strong> (Unicode) e <strong>JetGetDatabaseInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
