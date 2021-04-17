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
# <a name="desktop-app-printing"></a>Impressão de aplicativo de desktop

Esta seção descreve como imprimir de um programa nativo da área de trabalho do Windows.

## <a name="overview"></a>Visão geral

Para fornecer a melhor experiência de usuário ao imprimir a partir de um programa nativo do Windows, o programa deve ser projetado para imprimir a partir de um thread dedicado. Em um programa nativo do Windows, o programa é responsável por gerenciar eventos e mensagens da interface do usuário. As operações de impressão podem exigir períodos de computação intensa à medida que o conteúdo do aplicativo é renderizado para a impressora, o que pode impedir que o programa responda à interação do usuário se esse processamento for executado no mesmo thread que o processamento de eventos da interação do usuário.

Se você já estiver familiarizado com a forma de escrever um programa nativo do Windows multithread, vá diretamente para [como imprimir a partir de um aplicativo do Windows](how-to--print-from-a-windows-application.md) e saiba como adicionar funcionalidade de impressão ao seu programa.

### <a name="basic-windows-program-requirements"></a>Requisitos básicos do programa Windows

Para melhor desempenho e capacidade de resposta do programa, não execute o processamento do trabalho de impressão de um programa no thread que processa a interação do usuário.

Essa separação de impressão da interação do usuário influenciará o modo como o programa gerencia os dados do aplicativo. Você deve compreender totalmente essas implicações antes de começar a gravar o aplicativo. Os tópicos a seguir descrevem os requisitos básicos de tratamento de impressão em um thread separado de um programa.

### <a name="windows-program-basics"></a>Noções básicas do programa Windows

Um programa nativo do Windows deve fornecer o procedimento de janela principal para processar as mensagens de janela que ele recebe do sistema operacional. Cada janela em um programa do Windows tem uma função **WndProc** correspondente que processa essas mensagens de janela. O thread no qual essa função é executada é chamado de interface do usuário, ou thread da interface do usuário.

**Use os recursos para cadeias de caracteres.**  
Use os recursos de cadeia de caracteres do arquivo de recursos do programa em vez de constantes de cadeia de caracteres para cadeias que talvez precisem ser alteradas quando você oferecer suporte a outro idioma. Antes que um programa possa usar um recurso de cadeia de caracteres como uma cadeia de caracteres, o programa deve recuperar o recurso do arquivo de recurso e copiá-lo para um buffer de memória local. Isso requer alguma programação adicional no início, mas permite modificação, tradução e localização mais fáceis do programa no futuro.  
**Processar dados em etapas.**  
Processe o trabalho de impressão em etapas que podem ser interrompidas. Esse design possibilita que o usuário cancele uma operação de processamento longo antes de ser concluída e impede que o programa bloqueie outros programas que possam estar em execução ao mesmo tempo.  
**Use os dados do usuário do Windows.**  
Os aplicativos de impressão geralmente têm várias janelas e threads. Para manter os dados disponíveis entre threads e etapas de processamento sem usar variáveis estáticas, globais, referencie as estruturas de dados por um ponteiro de dados que faz parte da janela na qual elas são usadas.  


O exemplo de código a seguir mostra um ponto de entrada principal para um aplicativo de impressão. Este exemplo mostra como usar recursos de cadeia de caracteres em vez de constantes de cadeia de caracteres e também mostra o loop de mensagem principal que processa as mensagens de janela do programa.


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



### <a name="document-information"></a>Informações do documento

Programas nativos do Windows que são impressos devem ser projetados para processamento multi-threaded. Um dos requisitos de um design multi-threaded é proteger os elementos de dados do programa para que eles sejam seguros para que vários threads sejam usados ao mesmo tempo. Você pode proteger os elementos de dados usando objetos de sincronização e organizando os dados para evitar conflitos entre os threads. Ao mesmo tempo, o programa deve impedir alterações nos dados do programa enquanto ele está sendo impresso. O programa de exemplo usa várias técnicas de programação multi-threaded diferentes.

 **Eventos de sincronização**  
O programa de exemplo usa eventos, identificadores de thread e funções de espera para sincronizar o processamento entre o thread de impressão e o programa principal e indicar que os dados estão em uso.  
**Mensagens do Windows específicas do aplicativo**  
O programa de exemplo usa mensagens de janela específicas do aplicativo para tornar o programa mais compatível com outros programas nativos do Windows. Interromper o processamento em etapas menores e enfileirar essas etapas no loop de mensagem de janela torna mais fácil para o Windows gerenciar o processamento sem bloquear outros aplicativos que também podem estar em execução no computador.  
**estruturas de dados**  
O programa de exemplo não é escrito em um estilo orientado a objeto usando objetos e classes, embora agrupe elementos de dados em estruturas de dados. O exemplo não usa uma abordagem orientada a objeto para evitar a implicação de que uma abordagem é melhor ou pior do que a outra.  
Você pode usar as funções e estruturas de dados do programa de exemplo como um ponto de partida ao projetar seu programa. Independentemente de você decidir criar um programa orientado a objeto ou não, a consideração de design importante a ser lembrada é agrupar os elementos de dados relacionados para que você possa usá-los com segurança em threads diferentes, conforme necessário.  


### <a name="printer-device-context"></a>Contexto do dispositivo de impressora

Ao imprimir, talvez você queira renderizar o conteúdo a ser impresso em um contexto de dispositivo. [Como recuperar um contexto de dispositivo de impressora](retrieving-a-printer-device-context.md) descreve as diferentes maneiras que você pode obter um contexto de dispositivo de impressora.

## <a name="related-topics"></a>Tópicos relacionados



[Como imprimir a partir de um aplicativo do Windows](how-to--print-from-a-windows-application.md)


 

 



