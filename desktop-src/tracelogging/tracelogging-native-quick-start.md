---
title: RastreamentoLogging C/C++ Início Rápido
description: A seção a seguir descreve as etapas básicas necessárias para adicionar TraceLogging ao código nativo do modo de usuário.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: cb3734e3f314270e3d8082f5c9d25d38ce065829b94c659023950e5e2709047b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966495"
---
# <a name="tracelogging-cc-quick-start"></a>RastreamentoLogging C/C++ Início Rápido

A seção a seguir descreve as etapas básicas necessárias para adicionar TraceLogging ao código nativo do modo de usuário.

## <a name="prerequisites"></a>Pré-requisitos

-   Windows 10
-   Microsoft Visual Studio 2013
-   Windows 10 O SDK (Software Development Kit) é necessário para escrever um provedor de modo de usuário
-   Windows O WDK (Driver Kit) para Windows 10 é necessário para escrever um provedor de modo kernel

> [!IMPORTANT]
> Vincule advapi32.lib para compilar esses exemplos.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample.h

Este exemplo de header inclui as APIs TraceLogging e forward declara o handle do provedor que será usado para registrar eventos. Qualquer classe que deseje usar TraceLogging incluirá esse header e, em seguida, poderá iniciar o registro em log.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

O arquivo de header inclui TraceLoggingProvider.h, que define a API traceLogging nativa. Você deve incluir Windows.h primeiro porque ele define constantes usadas por TraceLoggingProvider.h.

O encaminhamento do arquivo de header declara o handle do provedor que você passará para `g_hMyComponentProvider` as APIs TraceLogging para registrar eventos. Esse handle precisa estar acessível a qualquer código que deseje usar TraceLogging.

[**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) é uma macro que cria um `extern const TraceLoggingHProvider` handle usando o nome que você fornece, que no exemplo acima é `g_hMyComponentProvider` . Você alocará a variável de lidar com o provedor real em um arquivo de código.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample.cpp

O exemplo a seguir registra o provedor, registra um evento e não registra o provedor.

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

O exemplo acima inclui SimpleTraceLoggingExample.h, que contém a variável de provedor global que seu código usará para registrar eventos.

A [**macro TRACELOGGING \_ DEFINE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) aloca armazenamento e define a variável de alça do provedor. O nome da variável que você fornece a essa macro deve corresponder ao nome usado na macro [**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) no arquivo de header. Esse handle permanecerá válido enquanto ele está no escopo.

### <a name="register-the-provider-handle"></a>Registrar o handle do provedor

Antes de usar o handle do provedor para registrar eventos, você deve chamar [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar o seu lidar com o provedor. Isso normalmente é feito em Main() ou DLLMain(), mas pode ser feito a qualquer momento, desde que preceda qualquer tentativa de registrar um evento. Se você registrar um evento antes de registrar o handle do provedor, nenhum erro ocorrerá, mas o evento não será registrado. O código a seguir do exemplo acima registra o handle do provedor.

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

A [**macro TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) ocupa até nove argumentos e é executada como várias instruções. Isso significa que os valores que estão sendo registrados não devem ser objetos temporários do C++. O nome do evento é armazenado no formato UTF-8. Você não deve usar `null` caracteres inseridos no evento ou em outros nomes de campo. Não há outros limites em caracteres permitidos.

Cada argumento após o nome do evento deve ser empacotado dentro de uma [macro Wrapper TraceLogging](tracelogging-wrapper-macros.md). Se você estiver usando o C++, poderá usar a macro wrapper para inferir automaticamente `TraceLoggingValue` o tipo do argumento. Se você estiver escrevendo seu driver em C, deverá usar macros de campo específicas do tipo, como `TraceLoggingInt32` `TraceLoggingUnicodeString` , , , `TraceLoggingString` etc. As macros wrapper TraceLogging são definidas em TraceLoggingProvider.h

Além de registrar eventos individuais em log, você também pode agrupar eventos por atividade usando as macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) ou [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) encontradas em TraceLoggingActivity.h. As atividades correlacionam eventos e são úteis para cenários que têm um início e um fim. Por exemplo, você pode usar uma atividade para medir um cenário que começa com o lançamento de um aplicativo, inclui o tempo necessário para a tela inicial ficar disponível e termina quando a tela inicial do aplicativo se torna visível.

As atividades capturam eventos individuais e aninham outras atividades que ocorrem entre o início e o fim dessa atividade. As atividades têm escopo por processo e devem ser passadas do thread para o thread para aninhar corretamente eventos multi-threaded.

O escopo de um handle de provedor é estritamente limitado ao módulo (arquivo DLL, EXE ou SYS) no qual ele é definido – o alça não deve ser passado para outras DLLs. Se uma [**macro TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) for invocada A.DLL usando um handle de provedor definido no B.DLL, isso poderá causar problemas. A maneira mais segura e eficiente de atender a esse requisito é sempre referenciar diretamente o handle do provedor global e nunca passar o handle do provedor como um parâmetro.

### <a name="unregister-the-provider"></a>Não registro do provedor

Quando terminar de registrar eventos em log, você deverá registrar o provedor TraceLogging. O código a seguir não registrou o provedor.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilidade

Dependendo de sua configuração, TraceLoggingProvider.h pode ser compatível com versões anteriores (compatível com o Windows Vista ou posterior) ou pode ser otimizado para versões posteriores do sistema operacional. TraceLoggingProvider.h usa WINVER (modo de usuário) e NTDDI_VERSION (modo kernel) para determinar se ele deve ser compatível com versões anteriores do sistema operacional ou ser otimizado para versões mais recentes do sistema operacional.

Para o modo de usuário, se você incluir <windows.h> antes de configurar o WINVER, <windows.h> definirá WINVER como a versão padrão do sistema operacional de destino do SDK. Se WINVER estiver definido como 0x602 ou superior, TraceLoggingProvider.h otimizará seu comportamento para Windows 8 (seu aplicativo não será executado em versões anteriores do Windows). Se você precisar que seu programa seja executado no Vista ou no Windows 7, certifique-se de definir WINVER com o valor apropriado antes de incluir <windows.h>.

Da mesma forma, se você incluir <wdm.h> antes de definir NTDDI_VERSION, <wdm.h> define NTDDI_VERSION como um valor padrão. Se NTDDI_VERSION estiver definido como 0x06040000 ou superior, TraceLoggingProvider.h otimizará seu comportamento para Windows 10 (o driver não funcionará em versões anteriores do Windows).

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

Para ver como capturar e exibir dados traceLogging usando as versões internas mais recentes do WPT (Ferramentas de Desempenho Windows), consulte Registrar e exibir eventos [traceLogging](tracelogging-record-and-display-tracelogging-events.md).

Consulte [Exemplos de rastreamento de C/C++](tracelogging-c-cpp-tracelogging-examples.md) para obter mais exemplos de TraceLogging do C++.

 

 




