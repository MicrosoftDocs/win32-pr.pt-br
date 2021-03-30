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
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/C++ Início Rápido

A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código nativo do modo de usuário.

## <a name="prerequisites"></a>Pré-requisitos

-   Windows 10
-   Microsoft Visual Studio 2013
-   O SDK (Software Development Kit) do Windows 10 é necessário para gravar um provedor de modo de usuário
-   O WDK (Kit de driver do Windows) para Windows 10 é necessário para gravar um provedor de modo kernel

> [!IMPORTANT]
> Vincule advapi32. lib para compilar esses exemplos.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample. h

Este cabeçalho de exemplo inclui as APIs TraceLogging e forward declara o identificador do provedor que será usado para registrar eventos. Qualquer classe que quiser usar TraceLogging incluirá esse cabeçalho e poderá iniciar o registro em log.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

O arquivo de cabeçalho inclui TraceLoggingProvider. h que define a API TraceLogging nativa. Você deve incluir o Windows. h primeiro porque ele define constantes usadas por TraceLoggingProvider. h.

O arquivo de cabeçalho encaminhar declara o identificador do provedor `g_hMyComponentProvider` que você passará para as APIs do TraceLogging para registrar eventos. Esse identificador precisa ser acessível a qualquer código que queira usar TraceLogging.

[**TRACELOGGING \_ DECLARAR \_ provedor**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) é uma macro que cria um `extern const TraceLoggingHProvider` identificador usando o nome que você fornece, que no exemplo acima é `g_hMyComponentProvider` . Você irá alocar a variável de identificador de provedor real em um arquivo de código.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample. cpp

O exemplo a seguir registra o provedor, registra um evento e cancela o registro do provedor.

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

O exemplo acima inclui SimpleTraceLoggingExample. h, que contém a variável de provedor global que seu código usará para registrar eventos.

A macro do [**\_ \_ provedor TRACELOGGING define**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) aloca armazenamento e define a variável de identificador do provedor. O nome da variável que você fornece para essa macro deve corresponder ao nome usado na macro [**do \_ \_ provedor TRACELOGGING declare**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) no arquivo de cabeçalho. Esse identificador permanecerá válido, desde que esteja no escopo.

### <a name="register-the-provider-handle"></a>Registrar o identificador do provedor

Antes de usar o identificador do provedor para registrar eventos, você deve chamar [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar seu identificador de provedor. Isso normalmente é feito em Main () ou DLLMain (), mas pode ser feito a qualquer momento, desde que ele preceda qualquer tentativa de registrar um evento. Se você registrar um evento antes de registrar o identificador do provedor, nenhum erro ocorrerá, mas o evento não será registrado. O código a seguir do exemplo acima registra o identificador do provedor.

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

### <a name="log-a-tracelogging-event"></a>Registrar um evento Tracelogging

Depois que o provedor é registrado, o código a seguir registra um evento simples.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

A macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) leva até 99 argumentos e é executada como várias instruções. Isso significa que os valores que estão sendo registrados não devem ser objetos temporários do C++. O nome do evento é armazenado no formato UTF-8. Você não deve usar caracteres inseridos `null` no evento ou em outros nomes de campo. Não há nenhum outro limite em caracteres permitidos.

Cada argumento após o nome do evento deve ser encapsulado dentro de uma [macro de invólucro TraceLogging](tracelogging-wrapper-macros.md). Se você estiver usando o C++, poderá usar a `TraceLoggingValue` macro wrapper para inferir automaticamente o tipo do argumento. Se você estiver escrevendo seu driver em C, deverá usar macros de campo específicas de tipo, como `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` etc. As macros do wrapper TraceLogging são definidas em TraceLoggingProvider. h

Além de registrar em log eventos únicos, você também pode agrupar eventos por atividade usando as macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) ou [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) encontradas em TraceLoggingActivity. h. As atividades correlacionam eventos e são úteis para cenários que têm um início e um fim. Por exemplo, você pode usar uma atividade para medir um cenário que começa com a inicialização de um aplicativo, inclui o tempo que leva para a tela inicial ficar disponível e termina quando a tela inicial do aplicativo se torna visível.

As atividades capturam eventos únicos e aninham outras atividades que ocorrem entre o início e o fim dessa atividade. As atividades têm escopo por processo e devem ser passadas de thread para thread para aninhar adequadamente eventos multi-threaded.

O escopo de um identificador de provedor é estritamente limitado ao módulo (arquivo DLL, EXE ou SYS) no qual ele é definido – o identificador não deve ser passado para outras DLLs. Se uma macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) for invocada no A.DLL usando um identificador de provedor definido em B.DLL, isso poderá causar problemas. A maneira mais segura e eficiente de atender a esse requisito é apenas referenciar diretamente o identificador do provedor global e nunca passar o identificador do provedor como um parâmetro.

### <a name="unregister-the-provider"></a>Cancelar o registro do provedor

Quando você terminar de registrar eventos, deverá cancelar o registro do provedor TraceLogging. O código a seguir cancela o registro do provedor.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilidade

Dependendo de sua configuração, o TraceLoggingProvider. h pode ser compatível com versões anteriores (compatível com o Windows Vista ou posterior), ou pode ser otimizado para versão posterior do so. TraceLoggingProvider. h usa WINVER (modo de usuário) e NTDDI_VERSION (modo kernel) para determinar se ele deve ser compatível com versões anteriores do sistema operacional ou ser otimizado para versões mais recentes do sistema operacional.

Para o modo de usuário, se você incluir <Windows. h> antes de configurar WINVER, <Windows. h> definirá WINVER para a versão do sistema operacional de destino padrão do SDK. Se WINVER estiver definido como 0x602 ou superior, TraceLoggingProvider. h otimizará seu comportamento para o Windows 8 (seu aplicativo não será executado em versões anteriores do Windows). Se você precisar que seu programa seja executado no Vista ou no Windows 7, certifique-se de definir WINVER para o valor apropriado antes de incluir <Windows. h>.

Da mesma forma, se você incluir <WDM. h> antes de definir NTDDI_VERSION, <WDM. h> definirá NTDDI_VERSION como um valor padrão. Se NTDDI_VERSION for definido como 0x06040000 ou superior, TraceLoggingProvider. h otimizará seu comportamento para o Windows 10 (o driver não funcionará em versões anteriores do Windows).

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

Para ver como capturar e exibir dados do TraceLogging usando as versões internas mais recentes das ferramentas de desempenho do Windows (WPT), consulte [gravar e exibir eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md).

Consulte [exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) para obter mais exemplos de Tracelogging de c++.

 

 




