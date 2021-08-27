---
description: O arquivo VBScript WiFilVer.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. O exemplo mostra como você pode usar um script para relatar ou atualizar as informações de versão, tamanho e idioma do arquivo.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gerenciar tamanhos e versões de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dcb5bec9b7fd24d7171efed9295479e56d979a3f7aa69352f2231d409417f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629037"
---
# <a name="manage-file-sizes-and-versions"></a>Gerenciar tamanhos e versões de arquivos

O arquivo VBScript WiFilVer.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) O exemplo mostra como você pode usar um script para relatar ou atualizar as informações de versão, tamanho e idioma do arquivo.

O exemplo também mostra as Windows do Instalador, como acessar um banco de dados do Windows Installer e o uso do seguinte:

-   [**Método Installer.OpenDatabase**](installer-opendatabase.md) do [ **Objeto do Instalador**](installer-object.md)
-   [**Propriedade Installer.FileAttributes**](installer-fileattributes.md)
-   [**Método Installer.FileHash**](installer-filehash.md)
-   [**Método Installer.FileVersion**](installer-fileversion.md)
-   [**Método Installer.LastErrorRecord**](installer-lasterrorrecord.md) do [ **Objeto do Instalador**](installer-object.md)
-   [**Método Database.OpenView**](database-openview.md)
-   [**Propriedade Database.SummaryInformation**](database-summaryinformation.md) do Objeto [ **de Banco de Dados**](database-object.md)
-   [**Método Session.DoAction**](session-doaction.md)
-   [**Session.Property**](session-session.md)
-   [**Propriedade Session.SourcePath**](session-sourcepath.md)
-   [**Propriedade Session.Mode**](session-mode.md) do [ **Objeto de Sessão**](session-object.md)
-   [**Propriedade Record.StringData**](record-stringdata.md)
-   [**Propriedade Record.IntegerData**](record-integerdata.md) do [ **Objeto de Registro**](record-object.md)

Usar este exemplo requer a versão CScript.exe ou WScript.exe do host Windows Script. Para usar CScript.exe executar este exemplo, digite um comando no prompt de comando usando a seguinte sintaxe:

**cscript WiFilVer.vbs \[ caminho para locais de origem \] \[ opcionais do banco de dados\]**

Também esteja ciente do seguinte:

-   A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados.
-   Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] .
-   O exemplo retornará um valor de 0 (zero) para êxito, 1 (um) se a ajuda for invocada e 2 (dois) se o script falhar.

Especifique Windows banco de dados do Instalador que você deseja atualizar, que deve estar localizado na raiz do arquivo de origem. No entanto, você pode especificar fontes para o banco de dados em locais separados. Se a origem for compactada, todos os arquivos serão abertos na raiz.

As opções a seguir podem ser especificadas em qualquer local na linha de comando.



| Opção                | Descrição                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *nenhuma opção especificada* | Exibir as informações do arquivo do banco de dados.                                            |
| /u                    | Atualize o tamanho do arquivo, a versão e as informações de idioma no banco de dados da origem. |



 

Para obter mais informações, [consulte exemplos Windows script do](windows-installer-scripting-examples.md) instalador do instalador e ferramentas Windows de desenvolvimento do [instalador.](windows-installer-development-tools.md)

 

 



