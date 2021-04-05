---
description: O arquivo VBScript WiFilVer.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. O exemplo mostra como você pode usar um script para relatar ou atualizar a versão do arquivo, o tamanho e as informações de idioma.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gerenciar tamanhos e versões de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647468"
---
# <a name="manage-file-sizes-and-versions"></a>Gerenciar tamanhos e versões de arquivo

O arquivo VBScript WiFilVer.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). O exemplo mostra como você pode usar um script para relatar ou atualizar a versão do arquivo, o tamanho e as informações de idioma.

O exemplo também mostra Windows Installer ações, como acessar um banco de dados do Windows Installer e o uso do seguinte:

-   Método [**Installer. OpenDatabase**](installer-opendatabase.md) do [ **objeto instalador**](installer-object.md)
-   Propriedade [**Installer. FileAttributes**](installer-fileattributes.md)
-   Método [**Installer. FileHash**](installer-filehash.md)
-   Método [**Installer. FileVersion**](installer-fileversion.md)
-   Método [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto instalador**](installer-object.md)
-   Método [**Database. OpenView**](database-openview.md)
-   Propriedade [**Database. SummaryInformation**](database-summaryinformation.md) do [ **objeto de banco de dados**](database-object.md)
-   Método [**Session. DoAction**](session-doaction.md)
-   [**Sessão. Propriedade**](session-session.md)
-   Propriedade [**Session. SourcePath**](session-sourcepath.md)
-   Propriedade [**Session. Mode**](session-mode.md) do [ **objeto Session**](session-object.md)
-   Propriedade [**Record. StringData**](record-stringdata.md)
-   Propriedade [**Record. IntegerData**](record-integerdata.md) do [ **objeto Record**](record-object.md)

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a seguinte sintaxe:

**cscript WiFilVer.vbs \[ caminho para os \] \[ locais de origem opcionais do banco de dados\]**

Lembre-se também do seguinte:

-   A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados.
-   Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .
-   O exemplo retorna um valor de 0 (zero) para êxito, 1 (um) se a ajuda for invocada e 2 (dois) se o script falhar.

Especifique o banco de dados Windows Installer que você deseja atualizar, que deve estar localizado na raiz do arquivo de origem. No entanto, você pode especificar fontes para o banco de dados em locais separados. Se a origem for compactada, todos os arquivos serão abertos na raiz.

As opções a seguir podem ser especificadas em qualquer local na linha de comando.



| Opção                | Descrição                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *nenhuma opção especificada* | Exibir as informações de arquivo do banco de dados.                                            |
| /u                    | Atualize o tamanho do arquivo, a versão e as informações de idioma no banco de dados da origem. |



 

Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) e [ferramentas de desenvolvimento de Windows Installer](windows-installer-development-tools.md).

 

 



