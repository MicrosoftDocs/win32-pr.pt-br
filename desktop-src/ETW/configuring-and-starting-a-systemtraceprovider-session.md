---
description: O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurando e iniciando uma sessão SystemTraceProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967440"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configurando e iniciando uma sessão SystemTraceProvider

O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior. No Windows 7 e no Windows Server 2008 R2, o SystemTraceProvider pode ser usado somente para a sessão do agente de log do NT kernel.

No Windows 8, no Windows Server 2012 e posterior, o SystemTraceProvider pode ser multiplexado em até 8 sessões de agente. Os dois primeiros slots para sessões de agente são reservados para o agente de log do kernel NT e para o agente de contexto de kernel circular.

Para obter mais informações sobre como usar a sessão do agente de log do NT kernel como um provedor de rastreamento, consulte [Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md).

Para habilitar o SystemTraceProvider para iniciar uma sessão que não seja o agente de log de kernel do NT, execute o comando a seguir.

**tracelog-iniciar MySession-f c: \\ Kernel1. etl-EFLAG proc \_ thread + Loader + CSWITCH**

Para habilitar programaticamente o SystemTraceProvider a iniciar uma sessão diferente do agente de log de kernel do NT, use as etapas a seguir.

-   Defina um nome de agente de log privado.

    **\#definir o \_ nome do agente de log privado \_ L "alguma sessão de rastreamento particular"**

-   No controlador, defina os seguintes membros da estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

    Defina **LOGFILEMODE** para **o \_ \_ modo de \_ agente \_** de log do sistema de rastreamento de eventos.

    Defina **loggername** para o agente de log privado, em vez do **\_ \_ nome do agente de log do kernel**.

    Verifique se o membro **Wnode. GUID** da estrutura [**de \_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) não está definido como **SystemTraceControlGuid**. Você deve atribuir um novo **GUID** a esse membro.

-   No consumidor, defina o membro **loggername** da estrutura de arquivo de [**\_ \_ log de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) para esse agente particular.

> [!Note]  
> Se você quiser que um processo não-administradores ou não TCB possa iniciar uma sessão de rastreamento de criação de perfil usando o SystemTraceProvider em nome de aplicativos de terceiros, será necessário conceder o privilégio de perfil de usuário e, em seguida, adicionar esse usuário ao **GUID** de sessão (criado para a sessão de agente) e ao **GUID** do provedor de rastreamento do sistema para habilitar o provedor de rastreamento do sistema. Para obter mais informações, consulte a função [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
