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
# <a name="a-database-and-patch-example"></a>Um exemplo de banco de dados e patch

Um aplicativo pode usar a função [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir um banco de dados de instalação novo ou existente (arquivo. msi) ou pacote de patch (arquivo. msp). O aplicativo verifica o valor de retorno de **MsiOpenDatabase** antes de usar o identificador de banco de dados.

Os exemplos a seguir usam as variáveis de tipo **PMSIHANDLE** definidas em MSI. h. É recomendável usar o tipo **PMSIHANDLE** porque o instalador fecha os objetos **PMSIHANDLE** à medida que eles saem do escopo, enquanto seu aplicativo deve fechar os objetos **MSIHANDLE** chamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Para obter mais informações [, consulte usar a seção PMSIHANDLE em vez de identificador](windows-installer-best-practices.md) no [Windows Installer práticas recomendadas](windows-installer-best-practices.md).

O exemplo a seguir abre um banco de dados, sample.msi, somente para leitura. O [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) só terá sucesso se sample.msi existir no diretório c: \\ Test. Após o êxito, o identificador de banco de dados retornado pode ser usado para consultar os dados no pacote de instalação usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



O exemplo a seguir abre o banco de dados para leitura e gravação. Se o aplicativo chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), todas as alterações feitas no banco de dados serão salvas. Se o aplicativo não chamar **MsiDatabaseCommit**, nenhuma alteração será feita no banco de dados.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



O exemplo a seguir usa um banco de dados existente, text.msi e cria um novo banco de dados, newtest.msi. As alterações feitas podem ser salvas no novo banco de dados chamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). O banco de dados existente especificado no parâmetro *szDatabasePath* não foi alterado.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



O exemplo a seguir abre um pacote de patches Windows Installer (arquivo. msp) somente para leitura. O identificador de patch retornado pode ser usado para determinar os gabinetes e transformar os subarmazenamentos incluídos no pacote de patch por consultas nas tabelas [ \_ fluxos](-streams-table.md) e [ \_ armazenamentos](-storages-table.md) .

**Windows Installer 2,0:** Sem suporte. A partir do Windows Installer 3,0, o aplicativo pode consultar a [tabela MsiPatchSequence](msipatchsequence-table.md) presente em um pacote de patch que usa as novas informações de sequenciamento de patch.


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



 

 



