---
description: Um aplicativo pode usar a função MsiOpenDatabase para abrir um banco de dados de instalação novo ou existente (arquivo .msi) ou pacote de patch (arquivo .msp).) O aplicativo verifica o valor de retorno de MsiOpenDatabase antes de usar o handle do banco de dados.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Um exemplo de banco de dados e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de816e471bbc3df4ec2970202130dba79267a06cb872e74734de322cba2d68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997026"
---
# <a name="a-database-and-patch-example"></a>Um exemplo de banco de dados e patch

Um aplicativo pode usar a [**função MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir um banco de dados de instalação novo ou existente (arquivo .msi) ou pacote de patch (arquivo .msp).) O aplicativo verifica o valor de retorno **de MsiOpenDatabase** antes de usar o handle do banco de dados.

Os exemplos a seguir usam as variáveis de tipo **PMSIHANDLE** definidas em msi.h. É recomendável usar o tipo **PMSIHANDLE** porque o instalador fecha objetos **PMSIHANDLE** à medida que eles ficam fora do escopo, enquanto seu aplicativo deve fechar objetos **MSIHANDLE** chamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Para obter mais [informações, consulte Usar PMSIHANDLE em vez da seção HANDLE](windows-installer-best-practices.md) na seção Práticas recomendadas do Windows [Instalador.](windows-installer-best-practices.md)

O exemplo a seguir abre um banco de dados, sample.msi, somente leitura. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) terá êxito somente se sample.msi existir no diretório de \\ teste c:. Após o sucesso, o alçamento de banco de dados retornado pode ser usado para consultar os dados no pacote de instalação usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



O exemplo a seguir abre o banco de dados para leitura e escrita. Se o aplicativo chamar [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), todas as alterações feitas no banco de dados serão salvas. Se o aplicativo não chamar **MsiDatabaseCommit**, nenhuma alteração será feita no banco de dados.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



O exemplo a seguir pega um banco de dados existente, text.msi, e cria um novo banco de dados, newtest.msi. Todas as alterações feitas podem ser salvas no novo banco de dados chamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). O banco de dados existente especificado no parâmetro *szDatabasePath* permanece inalterado.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



O exemplo a seguir abre um Windows patch do instalador (arquivo .msp) para somente leitura. O manipulador de patch retornado pode ser usado para determinar os gabinetes e transformar substorages incluídos no pacote de patch por consultas nas tabelas [ \_ Fluxos](-streams-table.md) [ \_ e Armazenamentos.](-storages-table.md)

**Windows Instalador 2.0:** Sem suporte. A partir do Windows 3.0, o aplicativo pode consultar a tabela [MsiPatchSequence](msipatchsequence-table.md) presente em um pacote de patch que usa as novas informações de sequenciamento de patch.


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



 

 



