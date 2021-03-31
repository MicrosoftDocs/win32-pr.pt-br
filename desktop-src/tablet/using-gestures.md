---
description: Visão geral do uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Usando gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920880"
---
# <a name="using-gestures"></a>Usando gestos

A plataforma do Tablet PC fornece o reconhecedor de gestos da Microsoft para dar suporte a gestos de aplicativo. Para obter uma lista de gestos com suporte pelo reconhecedor de gestos da Microsoft, consulte a tabela de gestos de aplicativo na enumeração [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) . O Tablet PC também dá suporte a gestos do sistema. Para obter uma lista de gestos do sistema com suporte pelo Tablet PC, consulte a tabela de gestos do sistema na enumeração [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .

## <a name="microsoft-gesture-recognizer"></a>Reconhecedor de gestos da Microsoft

Você pode empregar o reconhecedor de gestos da Microsoft usando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) do objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) . A definição da propriedade **CollectionMode** como modo misto (**InkAndGesture**) ou modo somente de gesto (**GestureOnly**) passa a tinta para o reconhecedor de gestos da Microsoft por padrão. Você pode empregar o reconhecedor de gestos da Microsoft com o controle [InkEdit](inkedit-control-reference.md) definindo a propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) como **InkAndGesture**. Você também pode usar o reconhecimento de gesto com o objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) adicionando um objeto [**GestureRecognizer**](gesturerecognizer-class.md) a uma de suas coleções de plug-ins.

No entanto, se os gestos que você deseja usar não forem suportados pela versão atual do reconhecedor de gestos da Microsoft, você poderá criar seu próprio reconhecedor e usá-lo em conjunto com o reconhecedor de gestos da Microsoft. Isso permite o suporte completo para os gestos em seu aplicativo.

O Tablet PC usa uma caneta para algumas ou todas as entradas. Isso torna extremamente fácil escrever tinta. A plataforma do Tablet PC fornece arquitetura para entrada à caneta que dá suporte a uma estrutura em camadas de gestos. Os gestos e o mapeamento são definidos para permitir que o usuário escreva e invoque gestos avançados em novas superfícies, enquanto reserva gestos que chamam mensagens de mouse tradicionais de outros aplicativos baseados no Windows.

A plataforma do Tablet PC apresenta dois níveis de gestos: gestos do sistema, também conhecidos como eventos do sistema e gestos do aplicativo. A arquitetura da caneta dá suporte a gestos do sistema e do aplicativo. Há suporte para gestos de aplicativo com traço único e vários traços.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gestos de aplicativo](application-gestures.md)
</dt> <dt>

[Gestos de movimentos](flicks-gestures.md)
</dt> <dt>

[Gestos do sistema](system-gestures.md)
</dt> </dl>

 

 



