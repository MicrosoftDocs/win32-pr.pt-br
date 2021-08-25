---
description: Ocasionalmente, ocorre uma situação em que uma mensagem não pode ser entregue com êxito ao destino pretendido, geralmente devido a um problema com o sistema ou a configuração.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Tratamento de erros em componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314ff367e656043746bb34bcb28b6c5a3dc8db9b86b58a482af45f684fb658c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991076"
---
# <a name="handling-errors-in-queued-components"></a>Tratamento de erros em componentes na fila

Ocasionalmente, ocorre uma situação em que uma mensagem não pode ser entregue com êxito ao destino pretendido, geralmente devido a um problema com o sistema ou a configuração. Por exemplo, a mensagem pode ser direcionada para uma fila que não existe ou a fila de destino pode não estar em um estado a ser recebido. O mover de mensagem é [](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) uma ferramenta que move todas as mensagens com falha no Enfiling de Mensagens de uma fila para outra para que possam ser recuperadas. O utilitário de movimentação de mensagens é um objeto de Automação que pode ser invocado com um VBScript.

## <a name="components-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência. Para usá-lo do Visual Basic, adicione uma referência à Biblioteca de Tipos de Serviços COM+.

> [!Note]  
> Para usar o objeto MessageMover, você deve ter o En enrosco de mensagens instalado em seu computador e o aplicativo especificado por AppName deve ter a fila habilitada. Para obter informações sobre como instalar o Enluamento de Mensagens, consulte Ajuda e suporte **no** menu Iniciar.

 


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



O código Visual Basic a seguir mostra como chamar a função MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



O caminho de origem da mensagem é a fila final da fila de fila. É a fila inominática, que é uma fila privada do Enfileiramento de Mensagens e é chamada \_ de fila inome do AppName. As mensagens serão movidas para aqui se a transação for anulada repetidamente quando tentada na quinta fila de novas tentativas. Com a ferramenta de movimentação de mensagens, você pode mover a mensagem de volta para a primeira fila, que é chamada AppName. Para obter mais informações sobre filas de repetir, consulte [Erros do lado do servidor.](server-side-errors.md)

Se os atributos de fila permitirem, o mover da mensagem move as mensagens em transição para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação. A ferramenta preserva todas as propriedades de mensagem que podem ser preservadas ao mover mensagens de uma fila para outra.

Se as mensagens são geradas por chamadas de Componentes Em Fila COM+, o utilitário de movimentação de mensagem preserva o identificador de segurança do chamador original à medida que move mensagens entre filas. Se as filas de destino e de origem são transacionais, toda a operação é feita em transição. Se as filas de origem ou de destino não são transacionais, a operação não é executado em uma transação. Uma falha inesperada (como uma falha) e a reinicialização de uma movimentação não transacional podem duplicar a mensagem que está sendo movida no momento da falha.

## <a name="cc"></a>C/C++

O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência. O método ErrorDescription é descrito em [Interpretando códigos de erro.](interpreting-error-codes.md)

> [!Note]  
> Para usar o objeto MessageMover, você deve ter o En enrosco de mensagens instalado em seu computador e o aplicativo especificado por AppName deve ter a fila habilitada. Para obter informações sobre como instalar o Enluamento de Mensagens, consulte Ajuda e suporte **no** menu Iniciar.

 


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



O caminho de origem da mensagem é a fila final da fila de fila. É a fila inominática, que é uma fila privada do Enfileiramento de Mensagens e é chamada \_ de fila inome do AppName. As mensagens serão movidas para aqui se a transação for anulada repetidamente quando tentada na quinta fila de novas tentativas. Com a ferramenta de movimentação de mensagens, você pode mover a mensagem de volta para a primeira fila, que é chamada AppName. Para obter mais informações sobre filas de repetir, consulte [Erros do lado do servidor.](server-side-errors.md)

Se os atributos de fila permitirem, o mover da mensagem move as mensagens em transição para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação. A ferramenta preserva todas as propriedades de mensagem que podem ser preservadas ao mover mensagens de uma fila para outra.

Se as mensagens são geradas por chamadas de Componentes Em Fila COM+, o utilitário de movimentação de mensagem preserva o identificador de segurança do chamador original à medida que move mensagens entre filas. Se as filas de destino e de origem são transacionais, toda a operação é feita em transição. Se as filas de origem ou de destino não são transacionais, a operação não é executado em uma transação. Uma falha inesperada (como uma falha) e a reinicialização de uma movimentação não transacional podem duplicar a mensagem que está sendo movida no momento da falha.

## <a name="remarks"></a>Comentários

O COM+ lida com anulações do lado do servidor (player) movendo a mensagem que está falhando em uma fila "final final" diferente, para que ela saia do caminho. O ouvinte e o player não podem fazer loop continuamente em uma mensagem anulada. Em muitos casos, a transação anulada pode ser corrigida por meio da ação no servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de componentes na fila](queued-components-errors.md)
</dt> </dl>

 

 



