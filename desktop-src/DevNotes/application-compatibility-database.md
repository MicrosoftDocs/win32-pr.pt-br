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
# <a name="application-compatibility-database"></a><span data-ttu-id="51d7a-103">Banco de dados de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="51d7a-103">Application Compatibility Database</span></span>

<span data-ttu-id="51d7a-104">A infraestrutura de compatibilidade usa um banco de dados para identificar problemas de compatibilidade de aplicativos e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="51d7a-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="51d7a-105">Esse banco de dados é um arquivo binário indexado com uma extensão. sdb.</span><span class="sxs-lookup"><span data-stu-id="51d7a-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="51d7a-106">A infraestrutura de compatibilidade fornece uma interface de programação para acessar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51d7a-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="51d7a-107">Problemas de compatibilidade podem ser abordados em uma base de aplicativo por aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="51d7a-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="51d7a-108">Cada aplicativo especificado no banco de dados contém um ou mais componentes que precisam de uma solução.</span><span class="sxs-lookup"><span data-stu-id="51d7a-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="51d7a-109">Os componentes são arquivos executáveis que geralmente são descritos usando seus atributos de arquivo (por exemplo, checksum).</span><span class="sxs-lookup"><span data-stu-id="51d7a-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="51d7a-110">O processo de pesquisa de banco de dados e determinação das soluções para cada aplicativo é chamado de *correspondência*.</span><span class="sxs-lookup"><span data-stu-id="51d7a-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="51d7a-111">Os atributos de arquivo e a presença de arquivos associados na pasta ou subpasta que contém o arquivo. exe podem ser usados para criar uma correspondência exclusiva.</span><span class="sxs-lookup"><span data-stu-id="51d7a-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="51d7a-112">Os arquivos associados são chamados de *arquivos correspondentes*.</span><span class="sxs-lookup"><span data-stu-id="51d7a-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="51d7a-113">Uma *marca* é um identificador exclusivo para as entradas e atributos no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51d7a-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="51d7a-114">O *tipo de marca* indica o formato dos dados associados à [**marca**](tag.md).</span><span class="sxs-lookup"><span data-stu-id="51d7a-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="51d7a-115">Por exemplo, **o \_ nome da marca** é do tipo **marca \_ tipo \_ STRINGREF**; os dados para o **\_ nome da marca** são uma cadeia de caracteres de nome.</span><span class="sxs-lookup"><span data-stu-id="51d7a-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="51d7a-116">Um *TagId* é um ponteiro para uma entrada em um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="51d7a-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="51d7a-117">Um *TAGREF* é um ponteiro para uma entrada que pode ser usada em vários bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="51d7a-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="51d7a-118">Os *atributos de arquivo* são metadados associados a um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="51d7a-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="51d7a-119">Esses atributos incluem o nome do arquivo, o tamanho do arquivo, a soma de verificação, a versão e a data.</span><span class="sxs-lookup"><span data-stu-id="51d7a-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="51d7a-120">Esses atributos são usados para determinar se um arquivo que está sendo carregado pelo sistema corresponde a uma entrada de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51d7a-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="51d7a-121">Portanto, esses atributos de arquivo também são chamados de *atributos correspondentes*.</span><span class="sxs-lookup"><span data-stu-id="51d7a-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="51d7a-122">Soluções</span><span class="sxs-lookup"><span data-stu-id="51d7a-122">Solutions</span></span>

<span data-ttu-id="51d7a-123">As soluções mais comuns aplicadas aos componentes de um aplicativo são AppHelp e AppFix.</span><span class="sxs-lookup"><span data-stu-id="51d7a-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="51d7a-124">Com AppHelp, uma notificação de mensagem localizada personalizada é exibida, normalmente quando o aplicativo é instalado ou iniciado.</span><span class="sxs-lookup"><span data-stu-id="51d7a-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="51d7a-125">Ele contém um breve texto que explica o problema de compatibilidade e fornece a opção para continuar a execução do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51d7a-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="51d7a-126">No entanto, alguns aplicativos apresentarão uma falha significativa para serem executados; AppHelp não dará ao usuário a opção de continuar a executar esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="51d7a-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="51d7a-127">Com o AppFix, os ganchos são instalados para APIs chamadas pelos componentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51d7a-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="51d7a-128">Esses ganchos apontam para funções de stub que podem ser chamadas em vez das funções do sistema (também conhecidas como *shims*).</span><span class="sxs-lookup"><span data-stu-id="51d7a-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="51d7a-129">As funções de stub executam operações necessárias para permitir que o aplicativo seja executado na versão instalada do Windows.</span><span class="sxs-lookup"><span data-stu-id="51d7a-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="51d7a-130">Cada função de stub pode, opcionalmente, chamar a função do sistema depois de concluir seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="51d7a-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="51d7a-131">Uma *camada de compatibilidade* ou *modo* contém um ou mais shims e sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="51d7a-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51d7a-132">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="51d7a-132">In this section</span></span>

-   [<span data-ttu-id="51d7a-133">**\_dados APPHELP**</span><span class="sxs-lookup"><span data-stu-id="51d7a-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="51d7a-134">**ATTRINFO**</span><span class="sxs-lookup"><span data-stu-id="51d7a-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="51d7a-135">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="51d7a-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="51d7a-136">**LOCALIZAR \_ informações**</span><span class="sxs-lookup"><span data-stu-id="51d7a-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="51d7a-137">**INDEXid**</span><span class="sxs-lookup"><span data-stu-id="51d7a-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="51d7a-138">**tipo de caminho \_**</span><span class="sxs-lookup"><span data-stu-id="51d7a-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="51d7a-139">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="51d7a-140">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="51d7a-141">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="51d7a-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="51d7a-142">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="51d7a-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="51d7a-143">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="51d7a-144">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="51d7a-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="51d7a-145">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="51d7a-146">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="51d7a-147">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="51d7a-148">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="51d7a-149">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="51d7a-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="51d7a-150">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="51d7a-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="51d7a-151">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="51d7a-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="51d7a-152">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="51d7a-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="51d7a-153">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="51d7a-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="51d7a-154">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="51d7a-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="51d7a-155">**SdbGetIndex**</span><span class="sxs-lookup"><span data-stu-id="51d7a-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="51d7a-156">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="51d7a-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="51d7a-157">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="51d7a-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="51d7a-158">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="51d7a-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="51d7a-159">**SdbGetTagFromTagID**</span><span class="sxs-lookup"><span data-stu-id="51d7a-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="51d7a-160">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="51d7a-161">**SdbIsStandardDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="51d7a-162">**SdbMakeIndexKeyFromString**</span><span class="sxs-lookup"><span data-stu-id="51d7a-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="51d7a-163">**SdbOpenApphelpDetailsDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="51d7a-164">**SdbOpenApphelpResourceFile**</span><span class="sxs-lookup"><span data-stu-id="51d7a-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="51d7a-165">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="51d7a-166">**SdbQueryDataExTagID**</span><span class="sxs-lookup"><span data-stu-id="51d7a-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="51d7a-167">**SDBQUERYRESULT**</span><span class="sxs-lookup"><span data-stu-id="51d7a-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="51d7a-168">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="51d7a-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="51d7a-169">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="51d7a-170">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="51d7a-171">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="51d7a-172">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="51d7a-173">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="51d7a-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="51d7a-174">**SdbReleaseDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="51d7a-175">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="51d7a-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="51d7a-176">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="51d7a-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="51d7a-177">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="51d7a-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="51d7a-178">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="51d7a-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="51d7a-179">**SdbTagToString**</span><span class="sxs-lookup"><span data-stu-id="51d7a-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="51d7a-180">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="51d7a-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="51d7a-181">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="51d7a-182">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="51d7a-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="51d7a-183">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="51d7a-184">**SdbWriteNULLTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="51d7a-185">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="51d7a-186">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="51d7a-187">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="51d7a-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="51d7a-188">**Tipos de banco de dados Shim**</span><span class="sxs-lookup"><span data-stu-id="51d7a-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="51d7a-189">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="51d7a-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="51d7a-190">**Tags**</span><span class="sxs-lookup"><span data-stu-id="51d7a-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="51d7a-191">**Tipos de marca**</span><span class="sxs-lookup"><span data-stu-id="51d7a-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="51d7a-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="51d7a-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="51d7a-193">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="51d7a-193">**TAGREF**</span></span>](tagref.md)

 

 



