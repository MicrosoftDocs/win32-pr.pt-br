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
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="7e8b4-103">Tratamento de erros em componentes na fila</span><span class="sxs-lookup"><span data-stu-id="7e8b4-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="7e8b4-104">Ocasionalmente, ocorre uma situação em que uma mensagem não pode ser entregue com êxito ao destino pretendido, geralmente devido a um problema com o sistema ou a configuração.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="7e8b4-105">Por exemplo, a mensagem pode ser direcionada para uma fila que não existe ou a fila de destino pode não estar em um estado para receber.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="7e8b4-106">O motor da mensagem é uma ferramenta que move todas as mensagens com falha do [serviço de enfileiramento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) de uma fila para outra para que elas possam ser repetidas.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="7e8b4-107">O utilitário de movimentação de mensagens é um objeto de automação que pode ser invocado com um VBScript.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="7e8b4-108">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="7e8b4-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="7e8b4-109">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="7e8b4-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7e8b4-110">Visual Basic</span></span>

<span data-ttu-id="7e8b4-111">O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="7e8b4-112">Para usá-lo de Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="7e8b4-113">Para usar o objeto MessageMover, você deve ter o enfileiramento de mensagens instalado no computador e o aplicativo especificado por AppName deve ter o enfileiramento habilitado.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="7e8b4-114">Para obter informações sobre como instalar o enfileiramento de mensagens, consulte ajuda e suporte no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="7e8b4-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


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



<span data-ttu-id="7e8b4-115">O código de Visual Basic a seguir mostra como chamar a função MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="7e8b4-116">O caminho de origem da mensagem é a fila de repouso final.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="7e8b4-117">É a fila inativa, que é uma fila de enfileiramento de mensagens particular e é chamada de AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="7e8b4-118">As mensagens serão movidas aqui se a transação for anulada repetidamente quando for tentada na quinta fila de repetição.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="7e8b4-119">Com a ferramenta de movimentação de mensagem, você pode mover a mensagem de volta para a primeira fila, que é chamada de AppName.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="7e8b4-120">Para obter mais informações sobre as filas de repetição, consulte [erros do lado do servidor](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7e8b4-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="7e8b4-121">Se os atributos de fila permitirem, o movimentador de mensagem moverá as mensagens de modo transitivo para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="7e8b4-122">A ferramenta preserva todas as propriedades de mensagem que podem ser mantidas ao mover mensagens de uma fila para outra.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="7e8b4-123">Se as mensagens forem geradas por chamadas de componentes em fila do COM+, o utilitário de movimentação de mensagens preservará o identificador de segurança do chamador original à medida que ele move mensagens entre filas.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="7e8b4-124">Se as filas de destino e de origem forem transacionais, toda a operação será feita em transição.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="7e8b4-125">Se as filas de origem ou de destino não forem transacionais, a operação não será executada em uma transação.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="7e8b4-126">Uma falha inesperada (como uma falha) e o reinício de uma movimentação não transacional pode duplicar a mensagem que está sendo movida no momento da falha.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="7e8b4-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e8b4-127">C/C++</span></span>

<span data-ttu-id="7e8b4-128">O código de exemplo a seguir mostra como criar um objeto MessageMover, definir as propriedades necessárias e iniciar a transferência.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="7e8b4-129">O método ErrorDescription é descrito em [interpretando códigos de erro](interpreting-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7e8b4-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="7e8b4-130">Para usar o objeto MessageMover, você deve ter o enfileiramento de mensagens instalado no computador e o aplicativo especificado por AppName deve ter o enfileiramento habilitado.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="7e8b4-131">Para obter informações sobre como instalar o enfileiramento de mensagens, consulte ajuda e suporte no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="7e8b4-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


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



<span data-ttu-id="7e8b4-132">O código C++ a seguir mostra como chamar a função MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


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



<span data-ttu-id="7e8b4-133">O caminho de origem da mensagem é a fila de repouso final.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="7e8b4-134">É a fila inativa, que é uma fila de enfileiramento de mensagens particular e é chamada de AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="7e8b4-135">As mensagens serão movidas aqui se a transação for anulada repetidamente quando for tentada na quinta fila de repetição.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="7e8b4-136">Com a ferramenta de movimentação de mensagem, você pode mover a mensagem de volta para a primeira fila, que é chamada de AppName.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="7e8b4-137">Para obter mais informações sobre as filas de repetição, consulte [erros do lado do servidor](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7e8b4-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="7e8b4-138">Se os atributos de fila permitirem, o movimentador de mensagem moverá as mensagens de modo transitivo para que as mensagens não sejam perdidas ou duplicadas em caso de falha durante a movimentação.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="7e8b4-139">A ferramenta preserva todas as propriedades de mensagem que podem ser mantidas ao mover mensagens de uma fila para outra.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="7e8b4-140">Se as mensagens forem geradas por chamadas de componentes em fila do COM+, o utilitário de movimentação de mensagens preservará o identificador de segurança do chamador original à medida que ele move mensagens entre filas.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="7e8b4-141">Se as filas de destino e de origem forem transacionais, toda a operação será feita em transição.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="7e8b4-142">Se as filas de origem ou de destino não forem transacionais, a operação não será executada em uma transação.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="7e8b4-143">Uma falha inesperada (como uma falha) e o reinício de uma movimentação não transacional pode duplicar a mensagem que está sendo movida no momento da falha.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e8b4-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e8b4-144">Remarks</span></span>

<span data-ttu-id="7e8b4-145">O COM+ manipula as anulações de servidor (Player) movendo a mensagem que está falhando em uma fila diferente de "repouso final", para desfazê-la.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="7e8b4-146">O ouvinte e o Player não podem fazer loop continuamente em uma mensagem anulada.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="7e8b4-147">Em muitos casos, a transação anulada pode ser corrigida executando uma ação no servidor.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e8b4-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e8b4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e8b4-149">Erros de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="7e8b4-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 



