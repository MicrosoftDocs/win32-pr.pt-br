---
description: o arquivo VBScript WiToAnsi.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar um arquivo Unicode para um arquivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224a9115da67848bd43aaceb7e5d8f529693558191e52a04de2e7645a4e60aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143370"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiar um arquivo Unicode para um arquivo ANSI

o arquivo VBScript WiToAnsi.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.

o uso deste exemplo requer a versão CScript.exe ou WScript.exe do Host de Script Windows. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiToAnsi.vbs \[ caminho para o caminho do arquivo Unicode \] \[ para o arquivo ANSI\]**

Especifique o arquivo de texto Unicode que está sendo convertido. Especifique o arquivo de texto ANSI que está sendo criado. Se nenhum arquivo ANSI for especificado, o arquivo Unicode será substituído.

para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). para utilitários de exemplo que não exigem Windows Host de Script, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



