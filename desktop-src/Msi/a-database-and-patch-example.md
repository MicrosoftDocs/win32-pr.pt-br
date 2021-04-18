---
description: Um aplicativo pode usar a função MsiOpenDatabase para abrir um banco de dados de instalação novo ou existente (arquivo. msi) ou pacote de patch (arquivo. msp). O aplicativo verifica o valor de retorno de MsiOpenDatabase antes de usar o identificador de banco de dados.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Um exemplo de banco de dados e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780967"
---
# <a name="a-database-and-patch-example"></a><span data-ttu-id="1825c-103">Um exemplo de banco de dados e patch</span><span class="sxs-lookup"><span data-stu-id="1825c-103">A Database and Patch Example</span></span>

<span data-ttu-id="1825c-104">Um aplicativo pode usar a função [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir um banco de dados de instalação novo ou existente (arquivo. msi) ou pacote de patch (arquivo. msp). O aplicativo verifica o valor de retorno de **MsiOpenDatabase** antes de usar o identificador de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1825c-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="1825c-105">Os exemplos a seguir usam as variáveis de tipo **PMSIHANDLE** definidas em MSI. h.</span><span class="sxs-lookup"><span data-stu-id="1825c-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="1825c-106">É recomendável usar o tipo **PMSIHANDLE** porque o instalador fecha os objetos **PMSIHANDLE** à medida que eles saem do escopo, enquanto seu aplicativo deve fechar os objetos **MSIHANDLE** chamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span><span class="sxs-lookup"><span data-stu-id="1825c-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="1825c-107">Para obter mais informações [, consulte usar a seção PMSIHANDLE em vez de identificador](windows-installer-best-practices.md) no [Windows Installer práticas recomendadas](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="1825c-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="1825c-108">O exemplo a seguir abre um banco de dados, sample.msi, somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1825c-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="1825c-109">O [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) só terá sucesso se sample.msi existir no diretório c: \\ Test.</span><span class="sxs-lookup"><span data-stu-id="1825c-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="1825c-110">Após o êxito, o identificador de banco de dados retornado pode ser usado para consultar os dados no pacote de instalação usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span><span class="sxs-lookup"><span data-stu-id="1825c-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="1825c-111">O exemplo a seguir abre o banco de dados para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="1825c-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="1825c-112">Se o aplicativo chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), todas as alterações feitas no banco de dados serão salvas.</span><span class="sxs-lookup"><span data-stu-id="1825c-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="1825c-113">Se o aplicativo não chamar **MsiDatabaseCommit**, nenhuma alteração será feita no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1825c-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="1825c-114">O exemplo a seguir usa um banco de dados existente, text.msi e cria um novo banco de dados, newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="1825c-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="1825c-115">As alterações feitas podem ser salvas no novo banco de dados chamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="1825c-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="1825c-116">O banco de dados existente especificado no parâmetro *szDatabasePath* não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="1825c-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="1825c-117">O exemplo a seguir abre um pacote de patches Windows Installer (arquivo. msp) somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1825c-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="1825c-118">O identificador de patch retornado pode ser usado para determinar os gabinetes e transformar os subarmazenamentos incluídos no pacote de patch por consultas nas tabelas [ \_ fluxos](-streams-table.md) e [ \_ armazenamentos](-storages-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1825c-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="1825c-119">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="1825c-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="1825c-120">A partir do Windows Installer 3,0, o aplicativo pode consultar a [tabela MsiPatchSequence](msipatchsequence-table.md) presente em um pacote de patch que usa as novas informações de sequenciamento de patch.</span><span class="sxs-lookup"><span data-stu-id="1825c-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



