---
title: Criando funções de retorno de chamada de status
description: Este tutorial descreve como criar uma função de retorno de chamada de status usada para monitorar o status de uma solicitação da Internet.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105791411"
---
# <a name="creating-status-callback-functions"></a>Criando funções de retorno de chamada de status

Este tutorial descreve como criar uma função de retorno de chamada de status usada para monitorar o status de uma solicitação da Internet.

As funções de retorno de chamada de status recebem retornos de chamada de status em quaisquer solicitações da Internet originadas de qualquer função WinINet que tenha passado um valor de contexto diferente de zero.


As etapas a seguir são necessárias para criar uma função de retorno de chamada de status:

1.  [Defina o valor do contexto.](#defining-the-context-value)
2.  [Crie a função de retorno de chamada de status.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Definindo o valor de contexto

O valor de contexto pode ser qualquer valor inteiro longo sem sinal. O ideal é que o valor de contexto identifique qual solicitação acabou de ser concluída e o local de todos os recursos associados, se necessário.

Uma das maneiras mais úteis de usar o valor de contexto é passar o endereço de uma estrutura e convertê-la em **um \_ PTR de DWORD**. A estrutura pode ser usada para armazenar informações sobre a solicitação, para que ela seja passada para a função de retorno de chamada de status.

A estrutura a seguir é um exemplo de um possível valor de contexto. Os membros da estrutura são escolhidos com a função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) em mente.


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



Neste exemplo, a função de retorno de chamada de status teria acesso ao identificador de janela, o que permitiria que ele exibesse uma interface do usuário. O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pode ser passado para outra função que pode baixar o recurso e uma matriz de caracteres que pode ser usada para passar informações sobre a solicitação.

Os membros da estrutura podem ser alterados para atender às necessidades de um aplicativo específico, portanto, não se sinta restritos por este exemplo.

### <a name="creating-the-status-callback-function"></a>Criando a função de retorno de chamada de status

A função de retorno de chamada de status deve seguir o formato de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback). Para fazer isso:

1.  Escreva uma declaração de função para sua função de retorno de chamada de status.

    O exemplo a seguir mostra uma declaração de exemplo.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Determine o que a função de retorno de chamada de status fará. Para aplicativos que estão fazendo chamadas assíncronas, a função de retorno de chamada de status deve tratar o valor de conclusão da solicitação de status da INTERNET \_ \_ , o \_ que indica que uma solicitação assíncrona foi concluída. A função de retorno de chamada de status também pode ser usada para acompanhar o progresso de uma solicitação da Internet.

    Em geral, funciona melhor usar uma instrução switch com *dwInternetStatus* como o valor de opção e os valores de status para as instruções Case. Dependendo dos tipos de funções que seu aplicativo está chamando, você pode ignorar alguns dos valores de status. Para obter uma definição dos diferentes valores de status, consulte a lista sob o parâmetro *dwInternetStatus* de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    A instrução switch a seguir é um exemplo de como lidar com os retornos de chamada de status.

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  Crie o código para manipular os valores de status.

    O código para lidar com cada um dos valores de status depende muito do uso pretendido da função de retorno de chamada de status. Para aplicativos que estão apenas acompanhando o progresso de uma solicitação, escrever uma cadeia de caracteres em uma caixa de listagem pode ser tudo o que você precisa. Para operações assíncronas, o código deve lidar com alguns dos dados retornados no retorno de chamada.

    A função de retorno de chamada de status a seguir usa uma função switch para determinar qual é o valor de status e cria uma cadeia de caracteres que inclui o nome do valor de status e a função anterior chamada, que é armazenada no membro szMemo da estrutura de contexto de solicitação \_ .

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  Use a função [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para definir a função de retorno de chamada de status no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para o qual você deseja receber retornos de chamada de status.

    O exemplo a seguir demonstra como definir uma função de retorno de chamada de status.

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando funções de retorno de chamada de status](creating-status-callback-functions.md)
</dt> <dt>

[**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 