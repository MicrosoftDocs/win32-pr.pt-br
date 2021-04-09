---
description: Se um aplicativo não chamar a função SymInitialize com o parâmetro fInvadeProcess definido como TRUE, ele deverá carregar símbolos para um módulo quando eles forem necessários.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Carregando um módulo de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088929"
---
# <a name="loading-a-symbol-module"></a>Carregando um módulo de símbolo

Se um aplicativo não chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) com o parâmetro *FInvadeProcess* definido como **true**, ele deverá carregar símbolos para um módulo quando eles forem necessários. Para carregar um módulo de símbolo sob demanda, o aplicativo pode chamar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) com um caminho completo para um nome de módulo. Quando o módulo for carregado, o manipulador de símbolo carregará os símbolos imediatamente ou adiará a carga, dependendo do conjunto de opções usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

O código a seguir carrega um módulo de símbolo. Observe que ele pressupõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolos](initializing-the-symbol-handler.md).


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



Observe que *szImageName* pode ser um caminho para qualquer módulo executável que tenha informações de depuração (. exe,. dll,. drv,. sys,. SCR,. cpl,. com). Além disso, *dwBaseAddr* é o endereço base do módulo de símbolo a ser carregado. Se esse valor for 0, o manipulador de símbolo obterá o endereço base do módulo de símbolo especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descarregando um módulo de símbolo](unloading-a-symbol-module.md)
</dt> </dl>

 

 



