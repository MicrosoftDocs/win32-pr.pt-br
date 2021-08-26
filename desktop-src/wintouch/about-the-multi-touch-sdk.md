---
title: sobre o Windows Touch
description: este tópico fornece uma breve visão geral de Windows toque.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Toque Software Development Kit
- Windows Toque, SDK
- Windows Toque, sobre
- Windows Toque, novos recursos
- Windows Toque, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3d86270ea6c43cc37c39a5d29282a0451dd38d312b996041dcd21f30de8d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881526"
---
# <a name="about-windows-touch"></a>sobre o Windows Touch

este tópico fornece uma breve visão geral de Windows toque.

novos elementos de hardware e API no sistema operacional Windows 7 fornecem aos aplicativos a capacidade de receber entrada de vários contatos. Isso dá a esses aplicativos a capacidade de detectar e responder a vários pontos de toque simultâneos na superfície visível do aplicativo. a funcionalidade para esse recurso no Windows 7 é fornecida por uma nova mensagem que relata e controla os toques. A nova mensagem, o [**WM \_ Touch**](wm-touchdown.md), relata a ação (para cima, para baixo, mover), posição e um identificador para pontos de toque. Windows as mensagens de toque são geradas por Windows e são entregues ao Windows que se registram para Windows entrada de toque.

Além da nova mensagem de entrada de toque, as mensagens de gesto foram adicionadas à lista existente de mensagens de janela. O suporte ao sistema de mensagens para gestos é habilitado por uma única nova mensagem de janela ([**\_ gesto do WM**](wm-gesture.md)) que é enviada ou postada para janelas de aplicativo apropriadas quando a entrada do usuário é reconhecida como um gesto. As funções de API dedicadas encapsulam os detalhes de criação e consumo desta mensagem. Isso é feito porque as informações associadas à mensagem podem ser alteradas no futuro sem interromper os aplicativos que já consomem essa mensagem.

além das mensagens de gesto, interfaces especializadas foram adicionadas ao SDK do Windows. Essas interfaces habilitam o suporte avançado para entrada por toque para que os desenvolvedores de aplicativos possam criar facilmente interfaces de usuário naturais. A interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpreta as mensagens do [**WM \_ Touch**](wm-touchdown.md) para gerar eventos que contêm informações de conversão, rotação e escala sobre uma coleção de pontos de toque. A interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pode ser usada em conjunto com a interface **IManipulationProcessor** para habilitar a animação e garantir que os objetos permaneçam na tela do usuário quando forem movidos.

os elementos de API para Windows Touch têm algumas semelhanças com o sdk do microsoft PixelSense (anteriormente conhecido como sdk do microsoft Surface), mas os aplicativos destinados ao microsoft PixelSense não são executados em computadores Windows Touch. além disso, os aplicativos destinados ao Windows Touch não são executados no Microsoft PixelSense.

algumas das funcionalidades do Windows Touch são incorporadas ao núcleo do Windows 7. Essa funcionalidade está disponível para os usuários sem a necessidade de os desenvolvedores habilitarem explicitamente o suporte. no entanto, para aproveitar ao máximo o Windows toque, os desenvolvedores devem usar a API de toque Windows. para começar a aprender como Windows Touch works, consulte o [guia de programação](programming-guide.md) ou comece com [a escolha da abordagem correta para Windows toque](choosing-the-right-approach-to-windows-touch.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da arquitetura](architectural-overview.md)
</dt> <dt>

[escolhendo a abordagem certa para Windows toque](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Tom](windows-touch-portal.md)
</dt> </dl>

 

 




