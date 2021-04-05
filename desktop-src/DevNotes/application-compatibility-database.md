---
description: A infraestrutura de compatibilidade usa um banco de dados para identificar problemas de compatibilidade de aplicativos e suas soluções.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Banco de dados de compatibilidade de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646266"
---
# <a name="application-compatibility-database"></a>Banco de dados de compatibilidade de aplicativos

A infraestrutura de compatibilidade usa um banco de dados para identificar problemas de compatibilidade de aplicativos e suas soluções. Esse banco de dados é um arquivo binário indexado com uma extensão. sdb. A infraestrutura de compatibilidade fornece uma interface de programação para acessar o banco de dados.

Problemas de compatibilidade podem ser abordados em uma base de aplicativo por aplicativo em tempo de execução. Cada aplicativo especificado no banco de dados contém um ou mais componentes que precisam de uma solução. Os componentes são arquivos executáveis que geralmente são descritos usando seus atributos de arquivo (por exemplo, checksum).

O processo de pesquisa de banco de dados e determinação das soluções para cada aplicativo é chamado de *correspondência*. Os atributos de arquivo e a presença de arquivos associados na pasta ou subpasta que contém o arquivo. exe podem ser usados para criar uma correspondência exclusiva. Os arquivos associados são chamados de *arquivos correspondentes*.

Uma *marca* é um identificador exclusivo para as entradas e atributos no banco de dados. O *tipo de marca* indica o formato dos dados associados à [**marca**](tag.md). Por exemplo, **o \_ nome da marca** é do tipo **marca \_ tipo \_ STRINGREF**; os dados para o **\_ nome da marca** são uma cadeia de caracteres de nome. Um *TagId* é um ponteiro para uma entrada em um banco de dados específico. Um *TAGREF* é um ponteiro para uma entrada que pode ser usada em vários bancos de dados.

Os *atributos de arquivo* são metadados associados a um arquivo no disco. Esses atributos incluem o nome do arquivo, o tamanho do arquivo, a soma de verificação, a versão e a data. Esses atributos são usados para determinar se um arquivo que está sendo carregado pelo sistema corresponde a uma entrada de banco de dados. Portanto, esses atributos de arquivo também são chamados de *atributos correspondentes*.

## <a name="solutions"></a>Soluções

As soluções mais comuns aplicadas aos componentes de um aplicativo são AppHelp e AppFix.

Com AppHelp, uma notificação de mensagem localizada personalizada é exibida, normalmente quando o aplicativo é instalado ou iniciado. Ele contém um breve texto que explica o problema de compatibilidade e fornece a opção para continuar a execução do aplicativo. No entanto, alguns aplicativos apresentarão uma falha significativa para serem executados; AppHelp não dará ao usuário a opção de continuar a executar esses aplicativos.

Com o AppFix, os ganchos são instalados para APIs chamadas pelos componentes do aplicativo. Esses ganchos apontam para funções de stub que podem ser chamadas em vez das funções do sistema (também conhecidas como *shims*). As funções de stub executam operações necessárias para permitir que o aplicativo seja executado na versão instalada do Windows. Cada função de stub pode, opcionalmente, chamar a função do sistema depois de concluir seu trabalho. Uma *camada de compatibilidade* ou *modo* contém um ou mais shims e sinalizadores.

## <a name="in-this-section"></a>Nesta seção

-   [**\_dados APPHELP**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**LOCALIZAR \_ informações**](find-info.md)
-   [**INDEXid**](indexid.md)
-   [**tipo de caminho \_**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNULLTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**Tipos de banco de dados Shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**Tags**](tag.md)
-   [**Tipos de marca**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



