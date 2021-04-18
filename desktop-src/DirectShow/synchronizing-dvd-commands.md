---
description: Sincronizando comandos de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizando comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785333"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="d7ec9-103">Sincronizando comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="d7ec9-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="d7ec9-104">Os comandos de DVD nem sempre são concluídos instantaneamente.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="d7ec9-105">Por esse motivo, alguns dos métodos em [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="d7ec9-106">Isso inclui métodos de reprodução, como **PlayTitle** e métodos de navegação de menu, como o **menu** de menus e **ReturnFromSubmenu**.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="d7ec9-107">Um método assíncrono retorna imediatamente, sem esperar que o comando seja concluído.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="d7ec9-108">Depois que o método retornar, outros eventos poderão impedir a conclusão do comando, mesmo se o método tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="d7ec9-109">O DirectShow fornece várias opções de sincronização de comandos, variando de nenhuma sincronização à sincronização completa usando eventos de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="d7ec9-110">Todos os métodos assíncronos têm um parâmetro *dwFlags* e um parâmetro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="d7ec9-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="d7ec9-111">O parâmetro *dwFlags* especifica o comportamento de sincronização e o parâmetro *ppCmd* retorna um ponteiro para um objeto de sincronização opcional.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="d7ec9-112">Comportamentos diferentes resultam de acordo com os valores que você fornece para esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="d7ec9-113">**Sem sincronização**</span><span class="sxs-lookup"><span data-stu-id="d7ec9-113">**No Synchronization**</span></span>

<span data-ttu-id="d7ec9-114">Para um aplicativo de reprodução de DVD básico, a melhor opção pode ser simplesmente ignorar problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="d7ec9-115">Ocasionalmente, um comando pode falhar ou a interface do usuário pode atrasar um pouco quando é atualizada, mas esses erros estarão na ordem de frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="d7ec9-116">Para emitir um comando sem sincronização, defina o sinalizador DVD \_ cmd \_ Flag \_ None no parâmetro *dwFlags* e defina o parâmetro *ppCmd* como **NULL**:</span><span class="sxs-lookup"><span data-stu-id="d7ec9-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="d7ec9-117">**Bloqueio**</span><span class="sxs-lookup"><span data-stu-id="d7ec9-117">**Blocking**</span></span>

<span data-ttu-id="d7ec9-118">Se você definir o \_ sinalizador de bloco de sinalizadores de DVD do EC \_ \_ \_ no parâmetro *dwFlags* , o método será bloqueado até que o comando seja concluído:</span><span class="sxs-lookup"><span data-stu-id="d7ec9-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="d7ec9-119">Na verdade, esse sinalizador transforma um método assíncrono em um método síncrono.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="d7ec9-120">A desvantagem é que sua interface do usuário será bloqueada se você chamar o método do thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="d7ec9-121">**Objeto de sincronização**</span><span class="sxs-lookup"><span data-stu-id="d7ec9-121">**Synchronization Object**</span></span>

<span data-ttu-id="d7ec9-122">Todos os métodos assíncronos podem retornar um objeto de sincronização, que você pode usar para aguardar até que o comando inicie ou termine.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="d7ec9-123">Para obter esse objeto, passe o endereço de um ponteiro [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) no parâmetro *ppCmd* :</span><span class="sxs-lookup"><span data-stu-id="d7ec9-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="d7ec9-124">Se o método tiver sucesso, ele retornará um novo objeto **IDvdCmd** .</span><span class="sxs-lookup"><span data-stu-id="d7ec9-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="d7ec9-125">O método [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) é bloqueado até que o comando comece e o método [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) seja bloqueado até que o comando termine.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="d7ec9-126">O valor de retorno indica o status do comando.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="d7ec9-127">O código a seguir é funcionalmente equivalente a definir o \_ sinalizador de bloco de sinalizadores de DVD do EC \_ \_ \_ , mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="d7ec9-128">Nesse caso, o método **PlayTitle** não bloqueia, mas os blocos de aplicativo chamando **WaitForEnd**.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="d7ec9-129">**Eventos de status de comando**</span><span class="sxs-lookup"><span data-stu-id="d7ec9-129">**Command Status Events**</span></span>

<span data-ttu-id="d7ec9-130">Se você definir o \_ sinalizador SendEvents de DVD cmd Flag \_ \_ no parâmetro *dwFlags* , o DVD Navigator enviará um evento de início de [**cmd de DVD EC quando o comando \_ \_ \_ for**](ec-dvd-cmd-start.md) iniciado e um evento de término de [**\_ cmd de DVD \_ \_ EC**](ec-dvd-cmd-end.md) quando o comando terminar.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="d7ec9-131">O parâmetro *lParam2* do evento é o valor de retorno HRESULT para o comando.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="d7ec9-132">O parâmetro *lParam1* do evento fornece uma maneira de obter o objeto de sincronização para o comando.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="d7ec9-133">Se você passar *lParam1* para o método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , o método retornará um ponteiro para a interface **IDvdCmd** do objeto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="d7ec9-134">Você pode usar essa interface para aguardar a conclusão do comando, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="d7ec9-135">No entanto, se você tiver passado **nulo** para o parâmetro *PpCmd* no método **IDvdControl2** original, o DVD Navigator não criará um objeto de sincronização e **GetCmdFromEvent** retornará e \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="d7ec9-136">O código a seguir mostra como usar eventos de status de comando sem objeto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="d7ec9-137">Observe que, sem um objeto de sincronização, você não pode saber qual comando está associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="d7ec9-138">O código a seguir mostra como usar eventos com o objeto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="d7ec9-139">A ideia é armazenar os objetos de sincronização em uma lista e, em seguida, comparar os ponteiros de objeto ao obter o evento de encerramento de cmd de [**\_ DVD EC \_ \_**](ec-dvd-cmd-start.md) ou de [**\_ \_ \_ fechamento de DVD EC**](ec-dvd-cmd-end.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ec9-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="d7ec9-140">**Liberando os buffers do navegador de DVD**</span><span class="sxs-lookup"><span data-stu-id="d7ec9-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="d7ec9-141">Durante a reprodução, o navegador de DVD armazena em buffer os dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="d7ec9-142">A quantidade de dados em buffer varia.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-142">The amount of buffered data varies.</span></span> <span data-ttu-id="d7ec9-143">Quando o navegador de DVD alterna para um novo vídeo, os dados que já estão no pipeline não são perdidos e, portanto, a transição é direta.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="d7ec9-144">Por padrão, quando o navegador de DVD emite um comando, ele não libera os dados que já estão no pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="d7ec9-145">Como resultado, pode haver alguma latência antes que você possa ver o efeito do comando, dependendo da quantidade de dados armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="d7ec9-146">Para aumentar a capacidade de resposta, você pode forçar a liberação do navegador de DVD definindo o \_ sinalizador de liberação do sinalizador de DVD cmd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d7ec9-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="d7ec9-147">Esse sinalizador pode ser combinado com qualquer um dos sinalizadores descritos anteriormente, usando um OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="d7ec9-148">Um efeito colateral da liberação é que algum vídeo pode ser perdido, portanto, não use esse sinalizador se você precisar garantir que não haja lacunas no vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7ec9-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7ec9-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7ec9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ec9-150">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="d7ec9-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



