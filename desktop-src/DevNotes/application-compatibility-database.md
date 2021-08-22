---
description: A infraestrutura de compatibilidade usa um banco de dados para identificar problemas de compatibilidade do aplicativo e suas soluções.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Banco de dados de compatibilidade do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787e8dbc9aa07bc8d466dae766c3fed406692dbd32e128123c4b37d9a7a5618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956155"
---
# <a name="application-compatibility-database"></a>Banco de dados de compatibilidade do aplicativo

A infraestrutura de compatibilidade usa um banco de dados para identificar problemas de compatibilidade do aplicativo e suas soluções. Esse banco de dados é um arquivo binário indexado com uma extensão .sdb. A infraestrutura de compatibilidade fornece uma interface de programação para acessar o banco de dados.

Os problemas de compatibilidade podem ser resolvidos por aplicativo em tempo de executar. Cada aplicativo especificado no banco de dados contém um ou mais componentes que precisam de uma solução. Os componentes são arquivos executáveis que geralmente são descritos usando seus atributos de arquivo (por exemplo, checksum).

O processo de busca de banco de dados e a determinação das soluções para cada aplicativo é chamado *de correspondente.* Os atributos de arquivo e a presença de arquivos associados na pasta ou na subpasta que contém o arquivo .exe podem ser usados para criar uma combinação exclusiva. Os arquivos associados são chamados de *arquivos correspondentes.*

Uma *TAG* é um identificador exclusivo para as entradas e atributos no banco de dados. O *tipo TAG* indica o formato dos dados associados à [**TAG.**](tag.md) Por exemplo, **TAG \_ NAME é do** tipo TAG TYPE **\_ \_ STRINGREF**; os dados para **TAG \_ NAME** são uma cadeia de caracteres de nome. Um *TAGID é* um ponteiro para uma entrada em um banco de dados específico. Um *TAGREF* é um ponteiro para uma entrada que pode ser usada em vários bancos de dados.

*Os atributos de* arquivo são metadados associados a um arquivo no disco. Esses atributos incluem o nome do arquivo, o tamanho do arquivo, a verificação, a versão e a data. Esses atributos são usados para determinar se um arquivo que está sendo carregado pelo sistema corresponde a uma entrada de banco de dados. Portanto, esses atributos de arquivo também são chamados *de atributos correspondentes.*

## <a name="solutions"></a>Soluções

As soluções mais comuns aplicadas aos componentes de um aplicativo são Apphelp e Appfix.

Com o Apphelp, uma notificação de mensagem localizada personalizada é exibida, normalmente quando o aplicativo é instalado ou iniciado. Ele contém um texto breve que explica o problema de compatibilidade e fornece a opção de continuar executando o aplicativo. No entanto, alguns aplicativos falharão drasticamente e poderão ser executados; O Apphelp não dará ao usuário a opção de continuar executando esses aplicativos.

Com Appfix, os ganchos são instalados para APIs chamadas pelos componentes do aplicativo. Esses ganchos apontam para funções de stub que podem ser chamadas em vez das funções do sistema (também conhecidas como *shimming*). As funções stub executam operações necessárias para permitir que o aplicativo seja executado na versão instalada do Windows. Cada função stub pode, opcionalmente, chamar a função do sistema depois de concluir seu trabalho. Uma *camada ou modo de* *compatibilidade* contém um ou mais shims e sinalizadores.

## <a name="in-this-section"></a>Nesta seção

-   [**APPHELP \_ DATA**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**ENCONTRAR \_ INFORMAÇÕES**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**TIPO DE \_ CAMINHO**](path-type.md)
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
-   [**Tipos de banco de dados shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**Tag**](tag.md)
-   [**Tipos de TAG**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



