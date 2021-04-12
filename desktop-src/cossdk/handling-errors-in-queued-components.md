---
description: Ocasionalmente, ocorre uma situação em que uma mensagem não pode ser entregue com êxito ao destino pretendido, geralmente devido a um problema com o sistema ou a configuração.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Tratamento de erros em componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501005"
---
# <a name="handling-errors-in-queued-components"></a>Tratamento de erros em componentes na fila

Ocasionalmente, ocorre uma situação em que uma mensagem não pode ser entregue com êxito ao destino pretendido, geralmente devido a um problema com o sistema ou a configuração. Por exemplo, a mensagem pode ser direcionada para uma fila que não existe ou a fila de destino pode não estar em um estado para receber. O motor da mensagem é uma ferramenta que move todas as mensagens com falha do [serviço de enfileiramento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) de uma fila para outra para que elas possam ser repetidas. O utilitário de movimentação de mensagens é um objeto de automação que pode ser invocado com um VBScript.

## <a name="components-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência. Para usá-lo de Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.

> [!Note]  
> Para usar o objeto MessageMover, você deve ter o enfileiramento de mensagens instalado no computador e o aplicativo especificado por AppName deve ter o enfileiramento habilitado. Para obter informações sobre como instalar o enfileiramento de mensagens, consulte ajuda e suporte no menu **Iniciar** .

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



O código de Visual Basic a seguir mostra como chamar a função MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



O caminho de origem da mensagem é a fila de repouso final. É a fila inativa, que é uma fila de enfileiramento de mensagens particular e é chamada de AppName \_ deadqueue. As mensagens serão movidas aqui se a transação for anulada repetidamente quando for tentada na quinta fila de repetição. Com a ferramenta de movimentação de mensagem, você pode mover a mensagem de volta para a primeira fila, que é chamada de AppName. Para obter mais informações sobre as filas de repetição, consulte [erros do lado do servidor](server-side-errors.md).

Se os atributos de fila permitirem, o movimentador de mensagem moverá as mensagens de modo transitivo para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação. A ferramenta preserva todas as propriedades de mensagem que podem ser mantidas ao mover mensagens de uma fila para outra.

Se as mensagens forem geradas por chamadas de componentes em fila do COM+, o utilitário de movimentação de mensagens preservará o identificador de segurança do chamador original à medida que ele move mensagens entre filas. Se as filas de destino e de origem forem transacionais, toda a operação será feita em transição. Se as filas de origem ou de destino não forem transacionais, a operação não será executada em uma transação. Uma falha inesperada (como uma falha) e o reinício de uma movimentação não transacional pode duplicar a mensagem que está sendo movida no momento da falha.

## <a name="cc"></a>C/C++

O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência. O método ErrorDescription é descrito em [interpretando códigos de erro](interpreting-error-codes.md).

> [!Note]  
> Para usar o objeto MessageMover, você deve ter o enfileiramento de mensagens instalado no computador e o aplicativo especificado por AppName deve ter o enfileiramento habilitado. Para obter informações sobre como instalar o enfileiramento de mensagens, consulte ajuda e suporte no menu **Iniciar** .

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



O código C++ a seguir mostra como chamar a função MyMessageMover.


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



O caminho de origem da mensagem é a fila de repouso final. É a fila inativa, que é uma fila de enfileiramento de mensagens particular e é chamada de AppName \_ deadqueue. As mensagens serão movidas aqui se a transação for anulada repetidamente quando for tentada na quinta fila de repetição. Com a ferramenta de movimentação de mensagem, você pode mover a mensagem de volta para a primeira fila, que é chamada de AppName. Para obter mais informações sobre as filas de repetição, consulte [erros do lado do servidor](server-side-errors.md).

Se os atributos de fila permitirem, o movimentador de mensagem moverá as mensagens de modo transitivo para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação. A ferramenta preserva todas as propriedades de mensagem que podem ser mantidas ao mover mensagens de uma fila para outra.

Se as mensagens forem geradas por chamadas de componentes em fila do COM+, o utilitário de movimentação de mensagens preservará o identificador de segurança do chamador original à medida que ele move mensagens entre filas. Se as filas de destino e de origem forem transacionais, toda a operação será feita em transição. Se as filas de origem ou de destino não forem transacionais, a operação não será executada em uma transação. Uma falha inesperada (como uma falha) e o reinício de uma movimentação não transacional pode duplicar a mensagem que está sendo movida no momento da falha.

## <a name="remarks"></a>Comentários

O COM+ manipula as anulações de servidor (Player) movendo a mensagem que está falhando em uma fila diferente de "repouso final", para desfazê-la. O ouvinte e o Player não podem fazer loop continuamente em uma mensagem anulada. Em muitos casos, a transação anulada pode ser corrigida executando uma ação no servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de componentes na fila](queued-components-errors.md)
</dt> </dl>

 

 



