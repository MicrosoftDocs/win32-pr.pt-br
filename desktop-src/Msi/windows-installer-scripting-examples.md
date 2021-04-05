---
description: Os componentes SDK do Windows para Windows Installer desenvolvedores contêm arquivos VBScript que mostram como a interface de automação do Windows Installer é usada para modificar os pacotes Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Exemplos de script de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921960"
---
# <a name="windows-installer-scripting-examples"></a>Exemplos de script de Windows Installer

Os [componentes SDK do Windows para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) contêm arquivos VBScript que mostram como a interface de automação do Windows Installer é usada para modificar os pacotes Windows Installer.

As amostras de script identificadas neste tópico não têm suporte da Microsoft Corporation e são fornecidas somente como uma referência potencialmente útil. A execução desses exemplos requer o Windows Script Host. Para obter mais informações sobre o Windows Script Host, consulte a seção [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) do SDK (Software Development Kit) do Microsoft Windows.



| Arquivo de script de exemplo | Descrição                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Listar produtos, propriedades, recursos e componentes](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importar arquivos](import-files.md)                                                                            |
| WiExport.vbs       | [Exportar arquivos](export-files.md)                                                                            |
| WiSubStg.vbs       | [Gerenciar subarmazenamentos](manage-substorages.md)                                                                |
| WiStream.vbs       | [Gerenciar fluxos binários](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Mesclar dois bancos de dados](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Gerar uma transformação](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Aplicar uma transformação](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Exibir uma transformação](view-a-transform.md) (somente cscript)                                                     |
| WiDiffDb.vbs       | [Exibir diferenças entre dois bancos de dados](view-differences-between-two-databases.md) (somente cscript)         |
| WiLstScr.vbs       | [Exibir o script do instalador](view-installer-script.md) (somente cscript)                                           |
| WiSumInf.vbs       | [Gerenciar informações de resumo](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Gerenciar configurações de política](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Gerenciar idioma e página de código](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copiar um arquivo Unicode para um arquivo ANSI](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Gerenciar tamanhos e versões de arquivo](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Gerar gabinete de arquivo](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Instruções SQL execute](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copiar arquivo ANSI em um campo de banco de dados](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Listar componentes](list-components.md)                                                                      |
| WiFeatur.vbs       | [Listar recursos](list-features.md)                                                                          |
| WiDialog.vbs       | [Visualizar interface do usuário](preview-user-interface.md)                                                        |



 

Todos esses scripts exibem uma tela de ajuda que descreve seus argumentos de linha de comando. Para exibir a tela de ajuda no Windows, clique duas vezes no arquivo. Para exibir a tela de ajuda em uma linha de comando, insira um? como o primeiro argumento ou digite menos argumentos do que o necessário. Os scripts retornam um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se em caso de falha.

Esses exemplos exigem que o Windows Script Host seja executado. Na verdade, o Windows Script Host é dois hosts:

-   CScript.exe é a versão que permite executar scripts do prompt de comando e fornece opções de linha de comando para definir propriedades de script.
-   WScript.exe é a versão do Windows Script Host que permite executar scripts do Windows. Para obter mais informações, consulte a seção [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) no SDK do Windows.

O utilitário Makecab.exe está incluído nos exemplos de aplicação de patches nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Para obter informações sobre o WMI, consulte [usando Windows Installer com o WMI](using-windows-installer-with-wmi.md).

 

 
