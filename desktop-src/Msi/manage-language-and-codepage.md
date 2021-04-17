---
description: O arquivo VBScript WiLangID.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gerenciar idioma e página de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789773"
---
# <a name="manage-language-and-codepage"></a>Gerenciar idioma e página de código

O arquivo VBScript WiLangID.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para acessar informações de idioma e página de código de um pacote. Para obter mais informações, consulte [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md) e [tratamento de página de código (Windows Installer)](code-page-handling-windows-installer-.md).

O exemplo demonstra o uso de:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propriedade SummaryInformation (objeto Database)**](database-summaryinformation.md) do [ **objeto Database**](database-object.md)

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiLangID.vbs o \[ valor da \] \[ palavra-chave Path \] to database \[\]**

Especifique o caminho para o banco de dados de Windows Installer. Para alterar um valor, especifique uma das seguintes palavras-chave seguidas pelo novo valor. Se nenhum valor for especificado, o exemplo retornará o valor atual.



| Palavra-chave      | Descrição                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pacote**  | As versões de idioma com suporte no banco de dados. Para obter informações, consulte Propriedade de [**Resumo do modelo**](template-summary.md) .                                                               |
| **Product**  | Idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados. Para obter informações, consulte Propriedade [**ProductLanguage**](productlanguage.md) . |
| **Codepage** | Página de código ANSI única para o pool de cadeias de caracteres. Para obter informações, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).                                       |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

Para obter mais informações, consulte [determinando a página de código](determining-an-installation-database-s-code-page.md) de um banco de dados de instalação e [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md).

 

 



