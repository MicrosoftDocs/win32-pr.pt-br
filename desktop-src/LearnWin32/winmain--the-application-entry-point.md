---
title: WinMain o ponto de entrada do aplicativo
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161941"
---
# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="cf665-103">WinMain: o ponto de entrada do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cf665-103">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="cf665-104">Cada programa do Windows inclui uma função de ponto de entrada denominada **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="cf665-104">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="cf665-105">Aqui está a assinatura para **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="cf665-105">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="cf665-106">Os quatro parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="cf665-106">The four parameters are:</span></span>

-   <span data-ttu-id="cf665-107">*HINSTANCE* é algo chamado "identificador para uma instância" ou "identificador para um módulo".</span><span class="sxs-lookup"><span data-stu-id="cf665-107">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="cf665-108">O sistema operacional usa esse valor para identificar o executável (EXE) quando ele é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="cf665-108">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="cf665-109">O identificador de instância é necessário para determinadas funções do Windows, por exemplo, para carregar ícones ou bitmaps.</span><span class="sxs-lookup"><span data-stu-id="cf665-109">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="cf665-110">*hPrevInstance* não tem significado.</span><span class="sxs-lookup"><span data-stu-id="cf665-110">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="cf665-111">Ele foi usado no Windows de 16 bits, mas agora é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="cf665-111">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="cf665-112">*pCmdLine* contém os argumentos de linha de comando como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf665-112">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="cf665-113">*nCmdShow* é um sinalizador que indica se a janela principal do aplicativo será minimizada, maximizada ou exibida normalmente.</span><span class="sxs-lookup"><span data-stu-id="cf665-113">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="cf665-114">A função retorna um valor **int** .</span><span class="sxs-lookup"><span data-stu-id="cf665-114">The function returns an **int** value.</span></span> <span data-ttu-id="cf665-115">O valor de retorno não é usado pelo sistema operacional, mas você pode usar o valor de retorno para transmitir um código de status para outro programa que você escreve.</span><span class="sxs-lookup"><span data-stu-id="cf665-115">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="cf665-116">**Winapi tenha** é a Convenção de chamada.</span><span class="sxs-lookup"><span data-stu-id="cf665-116">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="cf665-117">Uma *Convenção de chamada* define como uma função recebe parâmetros do chamador.</span><span class="sxs-lookup"><span data-stu-id="cf665-117">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="cf665-118">Por exemplo, ele define a ordem em que os parâmetros aparecem na pilha.</span><span class="sxs-lookup"><span data-stu-id="cf665-118">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="cf665-119">Apenas certifique-se de declarar sua função **wWinMain** , conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="cf665-119">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="cf665-120">A função **WinMain** é idêntica a **wWinMain**, exceto que os argumentos de linha de comando são passados como uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="cf665-120">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="cf665-121">A versão Unicode é preferida.</span><span class="sxs-lookup"><span data-stu-id="cf665-121">The Unicode version is preferred.</span></span> <span data-ttu-id="cf665-122">Você pode usar a função ANSI **WinMain** mesmo se compilar seu programa como Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf665-122">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="cf665-123">Para obter uma cópia Unicode dos argumentos de linha de comando, chame a função [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="cf665-123">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="cf665-124">Essa função retorna todos os argumentos em uma única cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf665-124">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="cf665-125">Se você quiser os argumentos como uma matriz de estilo *argv*, passe essa cadeia de caracteres para [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="cf665-125">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="cf665-126">Como o compilador sabe invocar **wWinMain** em vez da função **Main** padrão?</span><span class="sxs-lookup"><span data-stu-id="cf665-126">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="cf665-127">O que realmente acontece é que a Microsoft C Runtime Library (CRT) fornece uma implementação de **Main** que chama **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="cf665-127">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="cf665-128">O CRT faz algum trabalho adicional dentro do **principal**.</span><span class="sxs-lookup"><span data-stu-id="cf665-128">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="cf665-129">Por exemplo, todos os inicializadores estáticos são chamados antes de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="cf665-129">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="cf665-130">Embora você possa instruir o vinculador a usar uma função de ponto de entrada diferente, use o padrão se você vincular ao CRT.</span><span class="sxs-lookup"><span data-stu-id="cf665-130">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="cf665-131">Caso contrário, o código de inicialização do CRT será ignorado, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="cf665-131">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="cf665-132">(Por exemplo, objetos globais não serão inicializados corretamente.)</span><span class="sxs-lookup"><span data-stu-id="cf665-132">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="cf665-133">Aqui está uma função **WinMain** vazia.</span><span class="sxs-lookup"><span data-stu-id="cf665-133">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="cf665-134">Agora que você tem o ponto de entrada e entende algumas das convenções básicas de terminologia e codificação, você está pronto para criar um programa de janela completo.</span><span class="sxs-lookup"><span data-stu-id="cf665-134">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="cf665-135">Avançar</span><span class="sxs-lookup"><span data-stu-id="cf665-135">Next</span></span>

<span data-ttu-id="cf665-136">[Módulo 1. Seu primeiro programa do Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="cf665-136">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 