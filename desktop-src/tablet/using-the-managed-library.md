---
description: Visão geral da biblioteca gerenciada e observações sobre como usar a biblioteca gerenciada da plataforma do Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Usando a biblioteca gerenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105811593"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="e91c2-103">Usando a biblioteca gerenciada</span><span class="sxs-lookup"><span data-stu-id="e91c2-103">Using the Managed Library</span></span>

<span data-ttu-id="e91c2-104">A Common Language Runtime é a base da estrutura de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="e91c2-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="e91c2-105">Você pode considerar o Common Language Runtime como um agente que gerencia o código em tempo de execução, fornecendo serviços principais, como gerenciamento de memória, gerenciamento de threads e comunicação remota, ao mesmo tempo em que impõe a segurança de código estrita.</span><span class="sxs-lookup"><span data-stu-id="e91c2-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="e91c2-106">Na verdade, o conceito de gerenciamento de código é um princípio fundamental da Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="e91c2-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="e91c2-107">O código que tem como alvo o Common Language Runtime é conhecido como código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="e91c2-108">O código que não tem como alvo o Common Language Runtime é conhecido como código nativo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="e91c2-109">A biblioteca de classes de estrutura é uma coleção abrangente e orientada a objeto de classes reutilizáveis que você pode usar para desenvolver aplicativos que vão desde aplicativos tradicionais de linha de comando ou GUI (interface gráfica do usuário) até aplicativos com base nas inovações mais recentes fornecidas pelo ASP.NET e pelos serviços Web.</span><span class="sxs-lookup"><span data-stu-id="e91c2-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="e91c2-110">A biblioteca gerenciada do Tablet PC contém um conjunto de objetos gerenciados que estende a estrutura para fornecer suporte para entrada e saída de manuscrito no Tablet PC, bem como no intercâmbio de dados com outros computadores.</span><span class="sxs-lookup"><span data-stu-id="e91c2-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="e91c2-111">Exceções</span><span class="sxs-lookup"><span data-stu-id="e91c2-111">Exceptions</span></span>

<span data-ttu-id="e91c2-112">Os objetos de biblioteca gerenciados na API do Tablet PC encapsulam as implementações da biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="e91c2-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="e91c2-113">Quando o objeto ou controle da biblioteca COM subjacente retornar um erro, a API gerenciada lançará uma exceção Marshal. ThrowExceptionForHR que fornece os detalhes sobre a exceção COM interna.</span><span class="sxs-lookup"><span data-stu-id="e91c2-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="e91c2-114">Você pode consultar os valores HRESULT na referência da biblioteca COM para obter detalhes sobre os possíveis erros que podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="e91c2-115">Comparação de objetos</span><span class="sxs-lookup"><span data-stu-id="e91c2-115">Object Comparison</span></span>

<span data-ttu-id="e91c2-116">Para todos os objetos na biblioteca gerenciada da plataforma do Tablet PC, [**Equals**](/previous-versions/windows/) não é substituído para comparar corretamente dois objetos que são iguais.</span><span class="sxs-lookup"><span data-stu-id="e91c2-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="e91c2-117">A API (interface de programação de aplicativo) gerenciada não oferece suporte à comparação de objetos para igualdade, seja por meio da função **Equals** ou por meio do operador Equals (= =).</span><span class="sxs-lookup"><span data-stu-id="e91c2-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="e91c2-118">Ligando ao Microsoft.Ink.dll mais recente</span><span class="sxs-lookup"><span data-stu-id="e91c2-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="e91c2-119">O assembly de Microsoft.Ink.dll mais recente é uma substituição compatível para Microsoft.Ink.dll versão 1,0 e Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="e91c2-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="e91c2-120">Na maioria dos casos, você não precisa fazer nenhuma alteração em seus aplicativos que são distribuídos com os assemblies mais antigos.</span><span class="sxs-lookup"><span data-stu-id="e91c2-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="e91c2-121">No entanto, em alguns casos, você precisa instruir o carregador de Common Language Runtime a usar a biblioteca de vínculo dinâmico (DLL) mais recente sempre que as DLLs mais antigas tiverem sido referenciadas.</span><span class="sxs-lookup"><span data-stu-id="e91c2-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="e91c2-122">A única vez que você precisa associar explicitamente ao novo assembly usando a técnica a seguir é se seu aplicativo usa um componente que faz referência à versão 1,0 ou 1,5 do assembly em combinação com um componente que faz referência a um assembly de versão mais recente, como 1,7, e se esses componentes podem trocar dados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="e91c2-123">A melhor maneira de instruir o carregador de Common Language Runtime a usar a DLL mais recente é redirecionar as versões de assembly no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="e91c2-124">Você pode especificar que seu aplicativo use a versão mais recente do assembly colocando informações de associação de assembly no arquivo de configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="e91c2-125">Para obter mais informações sobre como redirecionar versões de assembly no nível do aplicativo, consulte [Redirecionando versões de assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), especificamente a seção "especificando a associação de assembly em arquivos de configuração".</span><span class="sxs-lookup"><span data-stu-id="e91c2-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="e91c2-126">Você precisará criar um arquivo de configuração no mesmo diretório que o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="e91c2-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="e91c2-127">O arquivo de configuração deve ter o mesmo nome que o executável, seguido pela extensão de arquivo. config.</span><span class="sxs-lookup"><span data-stu-id="e91c2-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="e91c2-128">Por exemplo, para um aplicativo, MyApp.exe, o arquivo de configuração deve ser o arquivo de MyApp.exe.config.</span><span class="sxs-lookup"><span data-stu-id="e91c2-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="e91c2-129">O arquivo de configuração usa um elemento [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) para forçar que todas as versões anteriores sejam mapeadas para a versão mais recente, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e91c2-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="e91c2-130">Para obter mais informações sobre arquivos de configuração, incluindo exemplos de como construir o linguagem XML (XML) para o arquivo de configuração, consulte o [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) e [redirecionando as versões do assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span><span class="sxs-lookup"><span data-stu-id="e91c2-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="e91c2-131">Os aplicativos criados com o Microsoft Windows XP Tablet PC Edition Development Kit 1,7 e versões posteriores são associados automaticamente à nova versão do assembly Microsoft. Ink.</span><span class="sxs-lookup"><span data-stu-id="e91c2-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="e91c2-132">Para obter mais informações sobre a associação de assembly, consulte [como o tempo de execução localiza assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span><span class="sxs-lookup"><span data-stu-id="e91c2-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="e91c2-133">Usar a política de aplicativo para associar ao assembly atualizado não funciona para aplicativos que usam a classe [divisória](/previous-versions/ms583616(v=vs.100)) ou a classe [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e91c2-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="e91c2-134">Os aplicativos que usam qualquer uma dessas classes devem continuar a usar Microsoft.Ink.15.dll ou ser recompilados depois de referenciar o assembly atualizado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="e91c2-135">Trabalhando com eventos</span><span class="sxs-lookup"><span data-stu-id="e91c2-135">Working with Events</span></span>

<span data-ttu-id="e91c2-136">Se o código dentro de um manipulador de eventos para qualquer um dos objetos gerenciados lançar uma exceção, a exceção não será entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e91c2-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="e91c2-137">Para garantir que as exceções sejam entregues, use blocos try-catch em seus manipuladores de eventos para eventos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="e91c2-138">Gerenciando formulários</span><span class="sxs-lookup"><span data-stu-id="e91c2-138">Managing Forms</span></span>

<span data-ttu-id="e91c2-139">A classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e suas classes base não definem um finalizador.</span><span class="sxs-lookup"><span data-stu-id="e91c2-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="e91c2-140">Para limpar seus recursos em um formulário, escreva uma subclasse que forneça um finalizador (por exemplo, o \# destruidor C usando o ~) que chama [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="e91c2-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="e91c2-141">Para fazer a limpeza, o finalizador substitui Dispose e, em seguida, chama a classe base Dispose.</span><span class="sxs-lookup"><span data-stu-id="e91c2-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="e91c2-142">Não faça referência a outros objetos que exigem o método [Finalize](/previous-versions/windows/) no método Dispose Quando o parâmetro booliano for **false**, pois esses objetos já podem ter sido finalizados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="e91c2-143">Para obter mais informações sobre como liberar recursos [, consulte Finalizar métodos e destruidores](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="e91c2-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="e91c2-144">Forms e RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="e91c2-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="e91c2-145">Os eventos [RecognizerContext](/previous-versions/ms552546(v=vs.100)) são executados em um thread diferente do thread em que o formulário está.</span><span class="sxs-lookup"><span data-stu-id="e91c2-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="e91c2-146">Os controles no Windows Forms são associados a um thread específico e não são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e91c2-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="e91c2-147">Portanto, você deve usar um dos métodos Invoke do controle para realizar marshaling da chamada para o thread apropriado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="e91c2-148">Quatro métodos em um controle são thread-safe: os métodos [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)e [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="e91c2-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="e91c2-149">Para todas as outras chamadas de método, use um desses métodos de invocação ao chamar de um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="e91c2-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="e91c2-150">Para obter mais informações sobre como usar esses métodos, consulte [manipulando controles de threads](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="e91c2-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="e91c2-151">Aguardando eventos</span><span class="sxs-lookup"><span data-stu-id="e91c2-151">Waiting for Events</span></span>

<span data-ttu-id="e91c2-152">O ambiente do Tablet PC é multithread.</span><span class="sxs-lookup"><span data-stu-id="e91c2-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="e91c2-153">Use a função [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) em vez de outros métodos de espera para permitir que as chamadas do COM (Component Object Model reentrantes) insiram seu MTA (multithreaded apartment) enquanto o aplicativo está aguardando um evento.</span><span class="sxs-lookup"><span data-stu-id="e91c2-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="e91c2-154">Usando coleções de traços de tinta</span><span class="sxs-lookup"><span data-stu-id="e91c2-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="e91c2-155">Instâncias de coleções de [traços](/previous-versions/ms552701(v=vs.100)) que são obtidas de um objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) não são coletadas pelo lixo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="e91c2-156">Para evitar um vazamento de memória, sempre que você estiver trabalhando com uma dessas coleções, use a instrução "using", conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="e91c2-157">Descartando objetos e controles gerenciados</span><span class="sxs-lookup"><span data-stu-id="e91c2-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="e91c2-158">Para evitar um vazamento de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer objeto do Tablet PC ou controle ao qual um manipulador de eventos foi anexado antes que o objeto ou controle saia do escopo.</span><span class="sxs-lookup"><span data-stu-id="e91c2-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="e91c2-159">Para melhorar o desempenho do seu aplicativo, descarte manualmente os seguintes objetos, controles e coleções quando não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="e91c2-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="e91c2-160">[Divisória](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="e91c2-161">[Tinta](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e91c2-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="e91c2-162">[Controles InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="e91c2-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="e91c2-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="e91c2-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e91c2-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="e91c2-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e91c2-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="e91c2-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="e91c2-168">[Traços](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e91c2-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="e91c2-169">O exemplo C a seguir \# demonstra alguns cenários em que o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) é usado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 