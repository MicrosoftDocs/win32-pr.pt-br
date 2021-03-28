---
description: A API do Shell fornece funções que você pode usar para gerenciar impressoras em rede. Se um arquivo tiver o verbo de impressão associado a ele, você poderá usar o comando ShellExecuteEx para imprimi-lo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gerenciando impressoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968001"
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

Se um tipo de arquivo tiver um comando de impressão associado a ele, você poderá imprimir o arquivo chamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) com **Print** como o verbo. Esse comando é geralmente o mesmo usado para o verbo **Open** , com a adição de um sinalizador para dizer ao aplicativo para imprimir o arquivo. Por exemplo, os arquivos. txt podem ser impressos pelo Microsoft WordPad. O verbo **Open** para um arquivo. txt, portanto, corresponderia a algo como o seguinte comando:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Quando você usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir um arquivo. txt, o WordPad abre o arquivo, o imprime e, em seguida, fecha, retornando o controle para o aplicativo. A função de exemplo a seguir usa um caminho totalmente qualificado e usa **ShellExecuteEx** para imprimi-lo, usando o comando Print associado à sua extensão de nome de arquivo.


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



 

 



