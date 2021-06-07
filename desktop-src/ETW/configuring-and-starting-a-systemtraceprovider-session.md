---
description: O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurando e iniciando uma sessão systemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386736"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configurando e iniciando uma sessão systemTraceProvider

O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior. No Windows 7 e no Windows Server 2008 R2, o SystemTraceProvider só pode ser usado para a sessão do NT Kernel Logger.

No Windows 8, no Windows Server 2012 e posterior, o SystemTraceProvider pode ser multiplexado para até 8 sessões de logger. Os dois primeiros slots para sessões de logger são reservados para o NT Kernel Logger e o Circular Kernel Context Logger .

Para obter mais informações sobre como usar a sessão do NT Kernel Logger como um provedor de rastreamento, consulte Configurando e iniciando a sessão do [NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).

No Windows 10 build do SDK 20348 e posterior, o SystemTraceProvider pode ser configurado por meio de provedores de sistema separados, que podem ser controlados com [EnableTraceEx2,](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) como provedores de eventos Rastreamento de Eventos para Windows padrão. Para ver uma lista completa de provedores de sistema, palavras-chave e grupos herdados [correspondentes,](system-providers.md) consulte Provedores de sistema

## <a name="enable-a-systemtraceprovider-session"></a>Habilitar uma sessão systemTraceProvider

Para habilitar o SystemTraceProvider a iniciar uma sessão diferente do NT Kernel Logger, execute o seguinte comando:

**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**

Para habilitar programaticamente o SystemTraceProvider para iniciar uma sessão diferente do NT Kernel Logger, use as etapas a seguir.

-   Defina um nome de logger privado.

    **\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**

-   No controlador, de definir os seguintes membros da estrutura [**EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

    De **definir LogFileMode** como **MODO DE \_ \_ LOGGGER DO SISTEMA \_ DE \_** RASTREAMENTO DE EVENTOS .

    De **configurar LoggerName** como um logger privado, em vez de **KERNEL \_ LOGGER \_ NAME**.

    Certifique-se **de que o membro Wnode.Guid** da estrutura EVENT TRACE [**\_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) não está definido **como SystemTraceControlGuid**. Você deve atribuir um **novo GUID** a esse membro.

-   No consumidor, de definido o **membro LoggerName** da estrutura [**EVENT TRACE \_ \_ LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) como esse loggger privado.

> [!Note]  
> Se você quiser que um processo não administrador ou não TCB seja capaz de iniciar uma sessão de rastreamento de criação de perfil usando o SystemTraceProvider em nome de aplicativos de terceiros, você precisará conceder o privilégio de perfil do usuário e, em seguida, adicionar esse usuário ao **GUID** de sessão (criado para a sessão do logger) e ao **GUID** do provedor de rastreamento do sistema para habilitar o provedor de rastreamento do sistema. Para obter mais informações, consulte [**a função EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)

 

## <a name="related-topics"></a>Tópicos relacionados

[Configurando e iniciando uma sessão de logger privado](configuring-and-starting-a-private-logger-session.md)

[Configurando e iniciando uma sessão do AutoLogger](configuring-and-starting-an-autologger-session.md)

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)

[Configurando e iniciando a sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md)

[Provedores de sistema](system-providers.md)

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)

 

 
