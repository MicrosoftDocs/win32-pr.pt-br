---
title: Sobre o Windows Touch
description: Este tópico fornece uma breve visão geral do Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, Software Development Kit
- Windows Touch, SDK
- Windows Touch, sobre
- Windows Touch, novos recursos
- Windows Touch, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915992"
---
# <a name="about-windows-touch"></a>Sobre o Windows Touch

Este tópico fornece uma breve visão geral do Windows Touch.

Novos elementos de hardware e API no sistema operacional Windows 7 fornecem aos aplicativos a capacidade de receber entrada de vários contatos. Isso dá a esses aplicativos a capacidade de detectar e responder a vários pontos de toque simultâneos na superfície visível do aplicativo. A funcionalidade para esse recurso no Windows 7 é fornecida por uma nova mensagem que relata e controla os toques. A nova mensagem, o [**WM \_ Touch**](wm-touchdown.md), relata a ação (para cima, para baixo, mover), posição e um identificador para pontos de toque. As mensagens do Windows Touch são geradas pelo Windows e são entregues ao Windows que se registram para entrada de toque do Windows.

Além da nova mensagem de entrada de toque, as mensagens de gesto foram adicionadas à lista existente de mensagens de janela. O suporte ao sistema de mensagens para gestos é habilitado por uma única nova mensagem de janela ([**\_ gesto do WM**](wm-gesture.md)) que é enviada ou postada para janelas de aplicativo apropriadas quando a entrada do usuário é reconhecida como um gesto. As funções de API dedicadas encapsulam os detalhes de criação e consumo desta mensagem. Isso é feito porque as informações associadas à mensagem podem ser alteradas no futuro sem interromper os aplicativos que já consomem essa mensagem.

Além das mensagens de gesto, interfaces especializadas foram adicionadas ao SDK do Windows. Essas interfaces habilitam o suporte avançado para entrada por toque para que os desenvolvedores de aplicativos possam criar facilmente interfaces de usuário naturais. A interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta as mensagens do [**WM \_ Touch**](wm-touchdown.md) para gerar eventos que contêm informações de conversão, rotação e escala sobre uma coleção de pontos de toque. A interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pode ser usada em conjunto com a interface **IManipulationProcessor** para habilitar a animação e garantir que os objetos permaneçam na tela do usuário quando forem movidos.

Os elementos de API para Windows Touch têm algumas semelhanças com o SDK do Microsoft PixelSense (anteriormente conhecido como SDK do Microsoft Surface), mas os aplicativos destinados ao Microsoft PixelSense não são executados em computadores Windows Touch. Além disso, os aplicativos que se destinam ao Windows Touch não são executados no Microsoft PixelSense.

Algumas das funcionalidades do Windows Touch são incorporadas ao núcleo do Windows 7. Essa funcionalidade está disponível para os usuários sem a necessidade de os desenvolvedores habilitarem explicitamente o suporte. No entanto, para aproveitar ao máximo o Windows Touch, os desenvolvedores devem usar a API de toque do Windows. Para começar a aprender como o Windows Touch funciona, consulte o [Guia de programação](programming-guide.md) ou comece com [a escolha da abordagem certa para o Windows Touch](choosing-the-right-approach-to-windows-touch.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da arquitetura](architectural-overview.md)
</dt> <dt>

[Escolhendo a abordagem certa para o Windows Touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Toque do Windows](windows-touch-portal.md)
</dt> </dl>

 

 




