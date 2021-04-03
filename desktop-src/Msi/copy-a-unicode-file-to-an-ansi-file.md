---
description: O arquivo VBScript WiToAnsi.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar um arquivo Unicode para um arquivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828876"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiar um arquivo Unicode para um arquivo ANSI

O arquivo VBScript WiToAnsi.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiToAnsi.vbs \[ caminho para o caminho do arquivo Unicode \] \[ para o arquivo ANSI\]**

Especifique o arquivo de texto Unicode que está sendo convertido. Especifique o arquivo de texto ANSI que está sendo criado. Se nenhum arquivo ANSI for especificado, o arquivo Unicode será substituído.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



