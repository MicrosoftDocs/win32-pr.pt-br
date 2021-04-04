---
title: TraceLogging C/C++ Início Rápido
description: A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código nativo do modo de usuário.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2020
ms.locfileid: "103917041"
---
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="08353-103">TraceLogging C/C++ Início Rápido</span><span class="sxs-lookup"><span data-stu-id="08353-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="08353-104">A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código nativo do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="08353-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08353-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="08353-105">Prerequisites</span></span>

-   <span data-ttu-id="08353-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="08353-106">Windows 10</span></span>
-   <span data-ttu-id="08353-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="08353-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="08353-108">O SDK (Software Development Kit) do Windows 10 é necessário para gravar um provedor de modo de usuário</span><span class="sxs-lookup"><span data-stu-id="08353-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="08353-109">O WDK (Kit de driver do Windows) para Windows 10 é necessário para gravar um provedor de modo kernel</span><span class="sxs-lookup"><span data-stu-id="08353-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08353-110">Vincule advapi32. lib para compilar esses exemplos.</span><span class="sxs-lookup"><span data-stu-id="08353-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="08353-111">SimpleTraceLoggingExample. h</span><span class="sxs-lookup"><span data-stu-id="08353-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="08353-112">Este cabeçalho de exemplo inclui as APIs TraceLogging e forward declara o identificador do provedor que será usado para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="08353-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="08353-113">Qualquer classe que quiser usar TraceLogging incluirá esse cabeçalho e poderá iniciar o registro em log.</span><span class="sxs-lookup"><span data-stu-id="08353-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="08353-114">O arquivo de cabeçalho inclui TraceLoggingProvider. h que define a API TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="08353-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="08353-115">Você deve incluir o Windows. h primeiro porque ele define constantes usadas por TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="08353-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="08353-116">O arquivo de cabeçalho encaminhar declara o identificador do provedor `g_hMyComponentProvider` que você passará para as APIs do TraceLogging para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="08353-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="08353-117">Esse identificador precisa ser acessível a qualquer código que queira usar TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="08353-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="08353-118">[**TRACELOGGING \_ DECLARAR \_ provedor**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) é uma macro que cria um `extern const TraceLoggingHProvider` identificador usando o nome que você fornece, que no exemplo acima é `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="08353-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="08353-119">Você irá alocar a variável de identificador de provedor real em um arquivo de código.</span><span class="sxs-lookup"><span data-stu-id="08353-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="08353-120">SimpleTraceLoggingExample. cpp</span><span class="sxs-lookup"><span data-stu-id="08353-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="08353-121">O exemplo a seguir registra o provedor, registra um evento e cancela o registro do provedor.</span><span class="sxs-lookup"><span data-stu-id="08353-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

<span data-ttu-id="08353-122">O exemplo acima inclui SimpleTraceLoggingExample. h, que contém a variável de provedor global que seu código usará para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="08353-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="08353-123">A macro do [**\_ \_ provedor TRACELOGGING define**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) aloca armazenamento e define a variável de identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="08353-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="08353-124">O nome da variável que você fornece para essa macro deve corresponder ao nome usado na macro [**do \_ \_ provedor TRACELOGGING declare**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="08353-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="08353-125">Esse identificador permanecerá válido, desde que esteja no escopo.</span><span class="sxs-lookup"><span data-stu-id="08353-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="08353-126">Registrar o identificador do provedor</span><span class="sxs-lookup"><span data-stu-id="08353-126">Register the provider handle</span></span>

<span data-ttu-id="08353-127">Antes de usar o identificador do provedor para registrar eventos, você deve chamar [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar seu identificador de provedor.</span><span class="sxs-lookup"><span data-stu-id="08353-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="08353-128">Isso normalmente é feito em Main () ou DLLMain (), mas pode ser feito a qualquer momento, desde que ele preceda qualquer tentativa de registrar um evento.</span><span class="sxs-lookup"><span data-stu-id="08353-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="08353-129">Se você registrar um evento antes de registrar o identificador do provedor, nenhum erro ocorrerá, mas o evento não será registrado.</span><span class="sxs-lookup"><span data-stu-id="08353-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="08353-130">O código a seguir do exemplo acima registra o identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="08353-130">The following code from the example above registers the provider handle.</span></span>

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="08353-131">Registrar um evento Tracelogging</span><span class="sxs-lookup"><span data-stu-id="08353-131">Log a Tracelogging event</span></span>

<span data-ttu-id="08353-132">Depois que o provedor é registrado, o código a seguir registra um evento simples.</span><span class="sxs-lookup"><span data-stu-id="08353-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="08353-133">A macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) leva até 99 argumentos e é executada como várias instruções.</span><span class="sxs-lookup"><span data-stu-id="08353-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="08353-134">Isso significa que os valores que estão sendo registrados não devem ser objetos temporários do C++.</span><span class="sxs-lookup"><span data-stu-id="08353-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="08353-135">O nome do evento é armazenado no formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="08353-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="08353-136">Você não deve usar caracteres inseridos `null` no evento ou em outros nomes de campo.</span><span class="sxs-lookup"><span data-stu-id="08353-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="08353-137">Não há nenhum outro limite em caracteres permitidos.</span><span class="sxs-lookup"><span data-stu-id="08353-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="08353-138">Cada argumento após o nome do evento deve ser encapsulado dentro de uma [macro de invólucro TraceLogging](tracelogging-wrapper-macros.md).</span><span class="sxs-lookup"><span data-stu-id="08353-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="08353-139">Se você estiver usando o C++, poderá usar a `TraceLoggingValue` macro wrapper para inferir automaticamente o tipo do argumento.</span><span class="sxs-lookup"><span data-stu-id="08353-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="08353-140">Se você estiver escrevendo seu driver em C, deverá usar macros de campo específicas de tipo, como `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` etc. As macros do wrapper TraceLogging são definidas em TraceLoggingProvider. h</span><span class="sxs-lookup"><span data-stu-id="08353-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="08353-141">Além de registrar em log eventos únicos, você também pode agrupar eventos por atividade usando as macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) ou [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) encontradas em TraceLoggingActivity. h.</span><span class="sxs-lookup"><span data-stu-id="08353-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="08353-142">As atividades correlacionam eventos e são úteis para cenários que têm um início e um fim.</span><span class="sxs-lookup"><span data-stu-id="08353-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="08353-143">Por exemplo, você pode usar uma atividade para medir um cenário que começa com a inicialização de um aplicativo, inclui o tempo que leva para a tela inicial ficar disponível e termina quando a tela inicial do aplicativo se torna visível.</span><span class="sxs-lookup"><span data-stu-id="08353-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="08353-144">As atividades capturam eventos únicos e aninham outras atividades que ocorrem entre o início e o fim dessa atividade.</span><span class="sxs-lookup"><span data-stu-id="08353-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="08353-145">As atividades têm escopo por processo e devem ser passadas de thread para thread para aninhar adequadamente eventos multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="08353-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="08353-146">O escopo de um identificador de provedor é estritamente limitado ao módulo (arquivo DLL, EXE ou SYS) no qual ele é definido – o identificador não deve ser passado para outras DLLs.</span><span class="sxs-lookup"><span data-stu-id="08353-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="08353-147">Se uma macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) for invocada no A.DLL usando um identificador de provedor definido em B.DLL, isso poderá causar problemas.</span><span class="sxs-lookup"><span data-stu-id="08353-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="08353-148">A maneira mais segura e eficiente de atender a esse requisito é apenas referenciar diretamente o identificador do provedor global e nunca passar o identificador do provedor como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="08353-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="08353-149">Cancelar o registro do provedor</span><span class="sxs-lookup"><span data-stu-id="08353-149">Unregister the provider</span></span>

<span data-ttu-id="08353-150">Quando você terminar de registrar eventos, deverá cancelar o registro do provedor TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="08353-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="08353-151">O código a seguir cancela o registro do provedor.</span><span class="sxs-lookup"><span data-stu-id="08353-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="08353-152">Compatibilidade</span><span class="sxs-lookup"><span data-stu-id="08353-152">Compatibility</span></span>

<span data-ttu-id="08353-153">Dependendo de sua configuração, o TraceLoggingProvider. h pode ser compatível com versões anteriores (compatível com o Windows Vista ou posterior), ou pode ser otimizado para versão posterior do so.</span><span class="sxs-lookup"><span data-stu-id="08353-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="08353-154">TraceLoggingProvider. h usa WINVER (modo de usuário) e NTDDI_VERSION (modo kernel) para determinar se ele deve ser compatível com versões anteriores do sistema operacional ou ser otimizado para versões mais recentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08353-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="08353-155">Para o modo de usuário, se você incluir <Windows. h> antes de configurar WINVER, <Windows. h> definirá WINVER para a versão do sistema operacional de destino padrão do SDK.</span><span class="sxs-lookup"><span data-stu-id="08353-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="08353-156">Se WINVER estiver definido como 0x602 ou superior, TraceLoggingProvider. h otimizará seu comportamento para o Windows 8 (seu aplicativo não será executado em versões anteriores do Windows).</span><span class="sxs-lookup"><span data-stu-id="08353-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="08353-157">Se você precisar que seu programa seja executado no Vista ou no Windows 7, certifique-se de definir WINVER para o valor apropriado antes de incluir <Windows. h>.</span><span class="sxs-lookup"><span data-stu-id="08353-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="08353-158">Da mesma forma, se você incluir <WDM. h> antes de definir NTDDI_VERSION, <WDM. h> definirá NTDDI_VERSION como um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="08353-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="08353-159">Se NTDDI_VERSION for definido como 0x06040000 ou superior, TraceLoggingProvider. h otimizará seu comportamento para o Windows 10 (o driver não funcionará em versões anteriores do Windows).</span><span class="sxs-lookup"><span data-stu-id="08353-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="08353-160">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="08353-160">Summary and next steps</span></span>

<span data-ttu-id="08353-161">Para ver como capturar e exibir dados do TraceLogging usando as versões internas mais recentes das ferramentas de desempenho do Windows (WPT), consulte [gravar e exibir eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="08353-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="08353-162">Consulte [exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) para obter mais exemplos de Tracelogging de c++.</span><span class="sxs-lookup"><span data-stu-id="08353-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




