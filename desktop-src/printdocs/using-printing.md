---
description: Esta seção descreve como imprimir de um programa nativo da área de trabalho do Windows.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Impressão de aplicativo de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748361"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="a6e67-103">Impressão de aplicativo de desktop</span><span class="sxs-lookup"><span data-stu-id="a6e67-103">Desktop App Printing</span></span>

<span data-ttu-id="a6e67-104">Esta seção descreve como imprimir de um programa nativo da área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6e67-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="a6e67-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a6e67-105">Overview</span></span>

<span data-ttu-id="a6e67-106">Para fornecer a melhor experiência de usuário ao imprimir a partir de um programa nativo do Windows, o programa deve ser projetado para imprimir a partir de um thread dedicado.</span><span class="sxs-lookup"><span data-stu-id="a6e67-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="a6e67-107">Em um programa nativo do Windows, o programa é responsável por gerenciar eventos e mensagens da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6e67-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="a6e67-108">As operações de impressão podem exigir períodos de computação intensa à medida que o conteúdo do aplicativo é renderizado para a impressora, o que pode impedir que o programa responda à interação do usuário se esse processamento for executado no mesmo thread que o processamento de eventos da interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6e67-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="a6e67-109">Se você já estiver familiarizado com a forma de escrever um programa nativo do Windows multithread, vá diretamente para [como imprimir a partir de um aplicativo do Windows](how-to--print-from-a-windows-application.md) e saiba como adicionar funcionalidade de impressão ao seu programa.</span><span class="sxs-lookup"><span data-stu-id="a6e67-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="a6e67-110">Requisitos básicos do programa Windows</span><span class="sxs-lookup"><span data-stu-id="a6e67-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="a6e67-111">Para melhor desempenho e capacidade de resposta do programa, não execute o processamento do trabalho de impressão de um programa no thread que processa a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6e67-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="a6e67-112">Essa separação de impressão da interação do usuário influenciará o modo como o programa gerencia os dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6e67-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="a6e67-113">Você deve compreender totalmente essas implicações antes de começar a gravar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6e67-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="a6e67-114">Os tópicos a seguir descrevem os requisitos básicos de tratamento de impressão em um thread separado de um programa.</span><span class="sxs-lookup"><span data-stu-id="a6e67-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="a6e67-115">Noções básicas do programa Windows</span><span class="sxs-lookup"><span data-stu-id="a6e67-115">Windows Program Basics</span></span>

<span data-ttu-id="a6e67-116">Um programa nativo do Windows deve fornecer o procedimento de janela principal para processar as mensagens de janela que ele recebe do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a6e67-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="a6e67-117">Cada janela em um programa do Windows tem uma função **WndProc** correspondente que processa essas mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="a6e67-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="a6e67-118">O thread no qual essa função é executada é chamado de interface do usuário, ou thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6e67-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="a6e67-119">**Use os recursos para cadeias de caracteres.**</span><span class="sxs-lookup"><span data-stu-id="a6e67-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="a6e67-120">Use os recursos de cadeia de caracteres do arquivo de recursos do programa em vez de constantes de cadeia de caracteres para cadeias que talvez precisem ser alteradas quando você oferecer suporte a outro idioma.</span><span class="sxs-lookup"><span data-stu-id="a6e67-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="a6e67-121">Antes que um programa possa usar um recurso de cadeia de caracteres como uma cadeia de caracteres, o programa deve recuperar o recurso do arquivo de recurso e copiá-lo para um buffer de memória local.</span><span class="sxs-lookup"><span data-stu-id="a6e67-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="a6e67-122">Isso requer alguma programação adicional no início, mas permite modificação, tradução e localização mais fáceis do programa no futuro.</span><span class="sxs-lookup"><span data-stu-id="a6e67-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="a6e67-123">**Processar dados em etapas.**</span><span class="sxs-lookup"><span data-stu-id="a6e67-123">**Process data in steps.**</span></span>  
<span data-ttu-id="a6e67-124">Processe o trabalho de impressão em etapas que podem ser interrompidas.</span><span class="sxs-lookup"><span data-stu-id="a6e67-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="a6e67-125">Esse design possibilita que o usuário cancele uma operação de processamento longo antes de ser concluída e impede que o programa bloqueie outros programas que possam estar em execução ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a6e67-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="a6e67-126">**Use os dados do usuário do Windows.**</span><span class="sxs-lookup"><span data-stu-id="a6e67-126">**Use window user data.**</span></span>  
<span data-ttu-id="a6e67-127">Os aplicativos de impressão geralmente têm várias janelas e threads.</span><span class="sxs-lookup"><span data-stu-id="a6e67-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="a6e67-128">Para manter os dados disponíveis entre threads e etapas de processamento sem usar variáveis estáticas, globais, referencie as estruturas de dados por um ponteiro de dados que faz parte da janela na qual elas são usadas.</span><span class="sxs-lookup"><span data-stu-id="a6e67-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="a6e67-129">O exemplo de código a seguir mostra um ponto de entrada principal para um aplicativo de impressão.</span><span class="sxs-lookup"><span data-stu-id="a6e67-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="a6e67-130">Este exemplo mostra como usar recursos de cadeia de caracteres em vez de constantes de cadeia de caracteres e também mostra o loop de mensagem principal que processa as mensagens de janela do programa.</span><span class="sxs-lookup"><span data-stu-id="a6e67-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="a6e67-131">Informações do documento</span><span class="sxs-lookup"><span data-stu-id="a6e67-131">Document Information</span></span>

<span data-ttu-id="a6e67-132">Programas nativos do Windows que são impressos devem ser projetados para processamento multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="a6e67-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="a6e67-133">Um dos requisitos de um design multi-threaded é proteger os elementos de dados do programa para que eles sejam seguros para que vários threads sejam usados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a6e67-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="a6e67-134">Você pode proteger os elementos de dados usando objetos de sincronização e organizando os dados para evitar conflitos entre os threads.</span><span class="sxs-lookup"><span data-stu-id="a6e67-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="a6e67-135">Ao mesmo tempo, o programa deve impedir alterações nos dados do programa enquanto ele está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="a6e67-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="a6e67-136">O programa de exemplo usa várias técnicas de programação multi-threaded diferentes.</span><span class="sxs-lookup"><span data-stu-id="a6e67-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="a6e67-137">**Eventos de sincronização**</span><span class="sxs-lookup"><span data-stu-id="a6e67-137">**Synchronization Events**</span></span>  
<span data-ttu-id="a6e67-138">O programa de exemplo usa eventos, identificadores de thread e funções de espera para sincronizar o processamento entre o thread de impressão e o programa principal e indicar que os dados estão em uso.</span><span class="sxs-lookup"><span data-stu-id="a6e67-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="a6e67-139">**Mensagens do Windows específicas do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="a6e67-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="a6e67-140">O programa de exemplo usa mensagens de janela específicas do aplicativo para tornar o programa mais compatível com outros programas nativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="a6e67-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="a6e67-141">Interromper o processamento em etapas menores e enfileirar essas etapas no loop de mensagem de janela torna mais fácil para o Windows gerenciar o processamento sem bloquear outros aplicativos que também podem estar em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="a6e67-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="a6e67-142">**estruturas de dados**</span><span class="sxs-lookup"><span data-stu-id="a6e67-142">**Data Structures**</span></span>  
<span data-ttu-id="a6e67-143">O programa de exemplo não é escrito em um estilo orientado a objeto usando objetos e classes, embora agrupe elementos de dados em estruturas de dados.</span><span class="sxs-lookup"><span data-stu-id="a6e67-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="a6e67-144">O exemplo não usa uma abordagem orientada a objeto para evitar a implicação de que uma abordagem é melhor ou pior do que a outra.</span><span class="sxs-lookup"><span data-stu-id="a6e67-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="a6e67-145">Você pode usar as funções e estruturas de dados do programa de exemplo como um ponto de partida ao projetar seu programa.</span><span class="sxs-lookup"><span data-stu-id="a6e67-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="a6e67-146">Independentemente de você decidir criar um programa orientado a objeto ou não, a consideração de design importante a ser lembrada é agrupar os elementos de dados relacionados para que você possa usá-los com segurança em threads diferentes, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a6e67-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="a6e67-147">Contexto do dispositivo de impressora</span><span class="sxs-lookup"><span data-stu-id="a6e67-147">Printer Device Context</span></span>

<span data-ttu-id="a6e67-148">Ao imprimir, talvez você queira renderizar o conteúdo a ser impresso em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6e67-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="a6e67-149">[Como recuperar um contexto de dispositivo de impressora](retrieving-a-printer-device-context.md) descreve as diferentes maneiras que você pode obter um contexto de dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="a6e67-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6e67-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6e67-150">Related topics</span></span>



[<span data-ttu-id="a6e67-151">Como imprimir a partir de um aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="a6e67-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



