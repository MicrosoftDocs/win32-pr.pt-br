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
# <a name="loading-a-symbol-module"></a><span data-ttu-id="169db-103">Carregando um módulo de símbolo</span><span class="sxs-lookup"><span data-stu-id="169db-103">Loading a Symbol Module</span></span>

<span data-ttu-id="169db-104">Se um aplicativo não chamar a função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) com o parâmetro *FInvadeProcess* definido como **true**, ele deverá carregar símbolos para um módulo quando eles forem necessários.</span><span class="sxs-lookup"><span data-stu-id="169db-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="169db-105">Para carregar um módulo de símbolo sob demanda, o aplicativo pode chamar a função [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) com um caminho completo para um nome de módulo.</span><span class="sxs-lookup"><span data-stu-id="169db-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="169db-106">Quando o módulo for carregado, o manipulador de símbolo carregará os símbolos imediatamente ou adiará a carga, dependendo do conjunto de opções usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="169db-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="169db-107">O código a seguir carrega um módulo de símbolo.</span><span class="sxs-lookup"><span data-stu-id="169db-107">The following code loads a symbol module.</span></span> <span data-ttu-id="169db-108">Observe que ele pressupõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolos](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="169db-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="169db-109">Observe que *szImageName* pode ser um caminho para qualquer módulo executável que tenha informações de depuração (. exe,. dll,. drv,. sys,. SCR,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="169db-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="169db-110">Além disso, *dwBaseAddr* é o endereço base do módulo de símbolo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="169db-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="169db-111">Se esse valor for 0, o manipulador de símbolo obterá o endereço base do módulo de símbolo especificado.</span><span class="sxs-lookup"><span data-stu-id="169db-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="169db-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="169db-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169db-113">Descarregando um módulo de símbolo</span><span class="sxs-lookup"><span data-stu-id="169db-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



