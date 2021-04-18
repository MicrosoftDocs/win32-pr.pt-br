---
description: Ocasionalmente, você pode precisar determinar se seu aplicativo está sendo executado em um Tablet PC porque talvez você queira que seus aplicativos aproveitem os recursos inerentes de tinta, reconhecimento e caneta.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinando se um PC é um Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793843"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Determinando se um PC é um Tablet PC

Ocasionalmente, você pode precisar determinar se seu aplicativo está sendo executado em um Tablet PC porque talvez você queira que seus aplicativos aproveitem os recursos inerentes de tinta, reconhecimento e caneta. Para ajudá-lo a determinar se seu aplicativo tem acesso aos recursos do Tablet PC, você pode usar a chamada à API do Windows GetSystemMetrics () conforme descrito neste tópico.

## <a name="client-side-applications"></a>Client-Side aplicativos

Você pode usar as seguintes técnicas para determinar se o seu código está sendo executado em um Tablet PC.

-   [Usando GetSystemMetrics (SM \_ Tablet)](/windows)
-   [Usando a presença de binários da plataforma Tablet](#using-the-presence-of-tablet-platform-binaries)
-   [Aplicativos baseados na Web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Usando GetSystemMetrics (SM \_ Tablet)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

No Microsoft Windows XP Tablet PC Edition, use a função GetSystemMetrics (SM \_ Tablet) para determinar se um computador é um Tablet PC. GetSystemMetrics (SM Tablet \_ ) foi projetado para retornar true em um computador que executa o Windows XP Notebook PC Edition.

### <a name="windows-vista"></a>Windows Vista

No Windows Vista, não há mais um SDK do Tablet PC distinto. O SDK do Windows agora contém uma seção chamada "Tablet PC e Touch Technology" e a lógica do GetSystemMetrics (SM Tablet \_ ) foi alterada para refletir isso. GetSystemMetrics (SM \_ Tablet) agora retornará true se todas as seguintes opções forem verdadeiras:

-   Há um digitalizador integrado, uma caneta ou um toque, no sistema.
-   O componente opcional do Tablet PC está instalado. Este componente contém recursos como painel de entrada do Tablet PC e diário do Windows.
-   O computador está licenciado para usar o componente opcional. As versões Premium do Windows Vista, como o Windows Vista Home Premium, o Windows Vista Small Business, o Windows Vista Professional, o Windows Vista Enterprise e o Windows Vista Ultimate, são licenciadas para usar o componente opcional.
-   O serviço de entrada do Tablet PC está em execução. O serviço de entrada do Tablet PC é um novo serviço do Windows Vista que controla a entrada do Tablet PC.

Com essa maior precisão, GetSystemMetrics (SM \_ Tablet) continua sendo a maneira recomendada de determinar se um computador que executa o Windows Vista é um Tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Usando a presença de binários da plataforma Tablet

No Windows XP Tablet PC Edition e no Windows Vista, você pode procurar a presença dos binários de tinta, como inkobj.dll e Microsoft.Ink.dll, e usar sua funcionalidade com suporte, se estiverem presentes.

No Windows Vista, os binários da plataforma Tablet PC são instalados em todas as versões de cliente por padrão. A funcionalidade de entrada e de tinta está disponível nessas versões. O reconhecimento está disponível apenas nas versões Premium do Windows Vista.

### <a name="web-based-applications"></a>Web-Based aplicativos

No Windows Vista, a cadeia de caracteres do agente do usuário relatada pelo Internet Explorer inclui "Tablet PC 2,0" se, de acordo com GetSystemMetrics (SM Tablet \_ ), o dispositivo for um Tablet PC.

No Windows XP Tablet PC Edition 2005, a cadeia de caracteres do agente do usuário inclui o Tablet PC 1,7. A cadeia de caracteres do agente do usuário é semelhante ao seguinte:

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Use esse valor para determinar se o computador cliente é um Tablet PC e dá suporte a controles de tinta baseados na Web.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
