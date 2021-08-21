---
description: A API do Shell fornece funções que você pode usar para gerenciar impressoras em rede. Se um arquivo tiver o verbo de impressão associado a ele, você poderá usar o comando ShellExecuteEx para imprimi-lo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gerenciando impressoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7086b360355d0ad85be440bc8bc9e330bfa6dd25793cc943d3aacdbaa0d4a8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719594"
---
# <a name="managing-printers"></a>Gerenciando impressoras

A API do Shell fornece funções que você pode usar para gerenciar impressoras em rede. Se um arquivo tiver o verbo de **impressão** associado a ele, você poderá usar o comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimi-lo.

-   [Gerenciamento de impressora](#printer-management)
-   [Imprimindo arquivos com ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Gerenciamento de impressora

Você pode gerenciar impressoras em um sistema com a função [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) . Essa função permite que você:

-   Instalar impressoras.
-   Abra Impressoras.
-   Obter propriedades da impressora.
-   Crie links de impressora.
-   Imprima uma página de teste.

## <a name="printing-files-with-shellexecuteex"></a>Imprimindo arquivos com ShellExecuteEx

Se um tipo de arquivo tiver um comando de impressão associado a ele, você poderá imprimir o arquivo chamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) com **Print** como o verbo. Esse comando é geralmente o mesmo usado para o verbo **Open** , com a adição de um sinalizador para dizer ao aplicativo para imprimir o arquivo. Por exemplo, .txt arquivos podem ser impressos pelo Microsoft WordPad. O verbo **Open** para um arquivo de .txt, portanto, corresponderia a algo como o seguinte comando:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Quando você usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir um arquivo de .txt, o WordPad abre o arquivo, o imprime e, em seguida, fecha, retornando o controle para o aplicativo. A função de exemplo a seguir usa um caminho totalmente qualificado e usa **ShellExecuteEx** para imprimi-lo, usando o comando Print associado à sua extensão de nome de arquivo.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



