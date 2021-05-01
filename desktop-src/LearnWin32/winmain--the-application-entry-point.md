---
<span data-ttu-id="5e0e7-101">Título: WinMain a descrição do ponto de entrada do aplicativo: WinMain: o ponto de entrada do aplicativo MS. AssetID: 389da5d4-d0f9-4339-BE6C-0f4fecc59316 MS. tópico: artigo MS. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="5e0e7-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="5e0e7-102">WinMain: o ponto de entrada do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5e0e7-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="5e0e7-103">Cada programa do Windows inclui uma função de ponto de entrada denominada **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="5e0e7-104">Aqui está a assinatura para **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="5e0e7-105">Os quatro parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="5e0e7-105">The four parameters are:</span></span>

-   <span data-ttu-id="5e0e7-106">*HINSTANCE* é algo chamado "identificador para uma instância" ou "identificador para um módulo".</span><span class="sxs-lookup"><span data-stu-id="5e0e7-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="5e0e7-107">O sistema operacional usa esse valor para identificar o executável (EXE) quando ele é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="5e0e7-108">O identificador de instância é necessário para determinadas funções do Windows, por exemplo, para carregar ícones ou bitmaps.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="5e0e7-109">*hPrevInstance* não tem significado.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="5e0e7-110">Ele foi usado no Windows de 16 bits, mas agora é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="5e0e7-111">*pCmdLine* contém os argumentos de linha de comando como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="5e0e7-112">*nCmdShow* é um sinalizador que indica se a janela principal do aplicativo será minimizada, maximizada ou exibida normalmente.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="5e0e7-113">A função retorna um valor **int** .</span><span class="sxs-lookup"><span data-stu-id="5e0e7-113">The function returns an **int** value.</span></span> <span data-ttu-id="5e0e7-114">O valor de retorno não é usado pelo sistema operacional, mas você pode usar o valor de retorno para transmitir um código de status para outro programa que você escreve.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="5e0e7-115">**Winapi tenha** é a Convenção de chamada.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="5e0e7-116">Uma *Convenção de chamada* define como uma função recebe parâmetros do chamador.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="5e0e7-117">Por exemplo, ele define a ordem em que os parâmetros aparecem na pilha.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="5e0e7-118">Apenas certifique-se de declarar sua função **wWinMain** , conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="5e0e7-119">A função **WinMain** é idêntica a **wWinMain**, exceto que os argumentos de linha de comando são passados como uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="5e0e7-120">A versão Unicode é preferida.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-120">The Unicode version is preferred.</span></span> <span data-ttu-id="5e0e7-121">Você pode usar a função ANSI **WinMain** mesmo se compilar seu programa como Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="5e0e7-122">Para obter uma cópia Unicode dos argumentos de linha de comando, chame a função [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="5e0e7-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="5e0e7-123">Essa função retorna todos os argumentos em uma única cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="5e0e7-124">Se você quiser os argumentos como uma matriz de estilo *argv*, passe essa cadeia de caracteres para [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="5e0e7-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="5e0e7-125">Como o compilador sabe invocar **wWinMain** em vez da função **Main** padrão?</span><span class="sxs-lookup"><span data-stu-id="5e0e7-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="5e0e7-126">O que realmente acontece é que a Microsoft C Runtime Library (CRT) fornece uma implementação de **Main** que chama **WinMain** ou **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="5e0e7-127">O CRT faz algum trabalho adicional dentro do **principal**.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="5e0e7-128">Por exemplo, todos os inicializadores estáticos são chamados antes de **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="5e0e7-129">Embora você possa instruir o vinculador a usar uma função de ponto de entrada diferente, use o padrão se você vincular ao CRT.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="5e0e7-130">Caso contrário, o código de inicialização do CRT será ignorado, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="5e0e7-131">(Por exemplo, objetos globais não serão inicializados corretamente.)</span><span class="sxs-lookup"><span data-stu-id="5e0e7-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="5e0e7-132">Aqui está uma função **WinMain** vazia.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="5e0e7-133">Agora que você tem o ponto de entrada e entende algumas das convenções básicas de terminologia e codificação, você está pronto para criar um programa de janela completo.</span><span class="sxs-lookup"><span data-stu-id="5e0e7-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="5e0e7-134">Avançar</span><span class="sxs-lookup"><span data-stu-id="5e0e7-134">Next</span></span>

<span data-ttu-id="5e0e7-135">[Módulo 1. Seu primeiro programa do Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="5e0e7-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
