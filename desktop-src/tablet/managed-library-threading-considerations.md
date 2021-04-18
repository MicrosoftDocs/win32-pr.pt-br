---
description: As seguintes considerações de Threading do Tablet PC são específicas para a biblioteca gerenciada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerações sobre Threading de biblioteca gerenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764405"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="da0dd-103">Considerações sobre Threading de biblioteca gerenciada</span><span class="sxs-lookup"><span data-stu-id="da0dd-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="da0dd-104">As seguintes considerações de Threading do Tablet PC são específicas para a biblioteca gerenciada.</span><span class="sxs-lookup"><span data-stu-id="da0dd-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="da0dd-105">Segurança de thread</span><span class="sxs-lookup"><span data-stu-id="da0dd-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="da0dd-106">Aplicativos STA e MTA</span><span class="sxs-lookup"><span data-stu-id="da0dd-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="da0dd-107">Considerações de threading de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="da0dd-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="da0dd-108">Considerações da área de transferência</span><span class="sxs-lookup"><span data-stu-id="da0dd-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="da0dd-109">Exceções nos manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="da0dd-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="da0dd-110">Descartando objetos e controles</span><span class="sxs-lookup"><span data-stu-id="da0dd-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="da0dd-111">APIs do StylusInput</span><span class="sxs-lookup"><span data-stu-id="da0dd-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="da0dd-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="da0dd-112">Thread-Safety</span></span>

<span data-ttu-id="da0dd-113">As classes de biblioteca gerenciada da plataforma do Tablet PC não são geralmente thread-safe.</span><span class="sxs-lookup"><span data-stu-id="da0dd-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="da0dd-114">As coleções a seguir são thread-safe no nível do membro; no entanto, essas coleções não garantem que um enumerador seja protegido se outro thread operar na coleção simultaneamente:</span><span class="sxs-lookup"><span data-stu-id="da0dd-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="da0dd-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="da0dd-116">[Cursores](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="da0dd-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="da0dd-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="da0dd-119">[Reconhecedores](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="da0dd-120">[Tablet](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="da0dd-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="da0dd-121">Aplicativos STA e MTA</span><span class="sxs-lookup"><span data-stu-id="da0dd-121">STA and MTA Applications</span></span>

<span data-ttu-id="da0dd-122">Os aplicativos gerenciados criados usando os assistentes contidos no Microsoft Visual Studio .NET são STA (single-threaded apartment) por padrão.</span><span class="sxs-lookup"><span data-stu-id="da0dd-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="da0dd-123">Você pode alterar o apartamento para seu aplicativo definindo o thread STA ou o atributo de thread MTA (multithreaded apartment) no ponto de entrada do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da0dd-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="da0dd-124">Se seu aplicativo for executado em um MTA, você deverá escrever código de thread-safe; no entanto, ao fazer isso, você pode melhorar certos problemas de desempenho de manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="da0dd-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="da0dd-125">Para obter mais informações sobre o thread STA e os atributos de thread MTA, consulte [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) Class e [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span><span class="sxs-lookup"><span data-stu-id="da0dd-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="da0dd-126">Considerações de threading de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="da0dd-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="da0dd-127">Os controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) estendem os controles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="da0dd-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="da0dd-128">Os controles de Windows Forms usam o modelo STA (single-threaded apartment) porque Windows Forms se baseiam em janelas nativas do Win32 que são inerentemente de thread único.</span><span class="sxs-lookup"><span data-stu-id="da0dd-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="da0dd-129">No código gerenciado, os controles de tinta devem ser criados no mesmo thread que o thread principal para o formulário.</span><span class="sxs-lookup"><span data-stu-id="da0dd-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="da0dd-130">Em um aplicativo STA, determinados eventos acontecem em um thread que não seja o thread da interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da0dd-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="da0dd-131">Ao chamar qualquer Windows Forms objeto ou controle, incluindo os controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) , de dentro de um manipulador de eventos do Tablet PC, use o método herdado [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) do objeto ou do controle.</span><span class="sxs-lookup"><span data-stu-id="da0dd-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="da0dd-132">A propriedade [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , herdada da classe Control, pode ser usada para determinar se isso é necessário.</span><span class="sxs-lookup"><span data-stu-id="da0dd-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="da0dd-133">Por exemplo, no manipulador de eventos a seguir para o evento de [reconhecimento](/previous-versions/ms829424(v=msdn.10)) , a propriedade [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) é testada e, se for **true**, o manipulador de eventos será invocado novamente a partir do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="da0dd-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="da0dd-134">Se você colocar um [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) no awebpagein em um navegador (consulte [controles da Web](web-controls.md)), ele será executado como um aplicativo Sta.</span><span class="sxs-lookup"><span data-stu-id="da0dd-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="da0dd-135">Para aplicativos Smart Client (consulte [Sem implantação de toque](no-touch-deployment.md)), o desenvolvedor tem total controle sobre o [seja ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="da0dd-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="da0dd-136">(O padrão é geralmente STA, mas pode ser MTA, dependendo da sua versão do CLR.) Para problemas de Threading que envolvem o [**RealTimeStylus**](realtimestylus-class.md), consulte [considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="da0dd-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="da0dd-137">Para obter mais informações sobre como chamar Windows Forms de um aplicativo MTA, consulte [exemplo de controle de Windows Forms multithread](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="da0dd-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="da0dd-138">Considerações da área de transferência</span><span class="sxs-lookup"><span data-stu-id="da0dd-138">Clipboard Considerations</span></span>

<span data-ttu-id="da0dd-139">O objeto [Clipboard](../dataxchg/clipboard.md) funciona apenas de um thread STA.</span><span class="sxs-lookup"><span data-stu-id="da0dd-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="da0dd-140">Ao tentar copiar ou colar da área de transferência de um thread que não seja STA, você obtém um [ThreadStateException](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="da0dd-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="da0dd-141">Se seu aplicativo for MTA, crie um thread STA para manipular as chamadas de método da área de transferência e alguns dos outros aspectos da interface do usuário do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="da0dd-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="da0dd-142">Exceções nos manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="da0dd-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="da0dd-143">Não é possível acionar exceções de dentro de manipuladores de eventos do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="da0dd-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="da0dd-144">Por exemplo, se um delegado de manipulador de eventos para um objeto ou uma coleção do Tablet PC tiver três manipuladores registrados e o primeiro lançar uma exceção, a seguinte sequência ocorrerá:</span><span class="sxs-lookup"><span data-stu-id="da0dd-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="da0dd-145">O primeiro manipulador é encerrado.</span><span class="sxs-lookup"><span data-stu-id="da0dd-145">The first handler exits.</span></span>
2.  <span data-ttu-id="da0dd-146">A exceção é perdida.</span><span class="sxs-lookup"><span data-stu-id="da0dd-146">The exception is lost.</span></span>
3.  <span data-ttu-id="da0dd-147">Os manipuladores restantes não são invocados.</span><span class="sxs-lookup"><span data-stu-id="da0dd-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="da0dd-148">Descartando objetos e controles</span><span class="sxs-lookup"><span data-stu-id="da0dd-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="da0dd-149">Para evitar um vazamento de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer objeto do Tablet PC ou controle ao qual um manipulador de eventos foi anexado antes que o objeto ou controle saia do escopo.</span><span class="sxs-lookup"><span data-stu-id="da0dd-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="da0dd-150">Para melhorar o desempenho em seu aplicativo, descarte manualmente qualquer objeto ou controle do Tablet PC que implemente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando o objeto ou o controle não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="da0dd-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="da0dd-151">APIs do StylusInput</span><span class="sxs-lookup"><span data-stu-id="da0dd-151">StylusInput APIs</span></span>

<span data-ttu-id="da0dd-152">Para obter informações sobre considerações de threading para o objeto [**RealTimeStylus**](realtimestylus-class.md) e as APIs (interfaces de programação de aplicativo) do StylusInput, consulte [considerações de threading para as APIs do StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="da0dd-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
