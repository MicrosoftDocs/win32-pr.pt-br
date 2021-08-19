---
description: Visão geral do uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Usando gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c4748dbf2638a57e005562fdec735ea6e87c27757d46549b7577f3bed7741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449236"
---
# <a name="using-gestures"></a>Usando gestos

A plataforma tablet pc fornece o reconhecedor de gestos da Microsoft para dar suporte a gestos de aplicativo. Para ver uma lista de gestos com suporte pelo reconhecedor de gestos da Microsoft, consulte a tabela de gestos do aplicativo na [**enumeração ApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) O Tablet PC também dá suporte a gestos do sistema. Para ver uma lista de gestos do sistema com suporte no Tablet PC, consulte a tabela de gestos do sistema na [**enumeração SystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

## <a name="microsoft-gesture-recognizer"></a>Reconhecedor de Gestos da Microsoft

Você pode empregar o reconhecedor de gestos da Microsoft usando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) do objeto [**InkCollector,**](inkcollector-class.md) o [**objeto InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture.](inkpicture-control-reference.md) Definir a **propriedade CollectionMode** para o modo misto (**InkAndGesture**) ou o modo somente gesto (**GestureOnly**) passa tinta para o reconhecedor de gestos da Microsoft por padrão. Você pode empregar o reconhecedor de gestos da Microsoft com o [controle InkEdit](inkedit-control-reference.md) definindo a propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) como **InkAndGesture.** Você também pode usar o reconhecimento de gestos com o objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) adicionando um objeto [**GestureRecognizer**](gesturerecognizer-class.md) a uma de suas coleções de plug-in.

No entanto, se os gestos que você deseja usar não são suportados pela versão atual do reconhecedor de gestos da Microsoft, você pode criar seu próprio reconhecedor e usá-lo em conjunto com o reconhecedor de gestos da Microsoft. Isso permite suporte completo para os gestos em seu aplicativo.

O Tablet PC usa uma caneta para algumas ou todas as entradas. Isso torna extremamente fácil escrever tinta. A plataforma Tablet PC oferece arquitetura para entrada de caneta que dá suporte a uma estrutura em camadas de gestos. Gestos e mapeamento são definidos para permitir que o usuário escreva e invoque gestos avançados em novas superfícies, ao mesmo tempo que reserva gestos que invocam mensagens tradicionais do mouse de outros aplicativos baseados Windows aplicativos.

A plataforma Tablet PC apresenta dois níveis de gestos: gestos do sistema, também conhecidos como eventos do sistema e gestos de aplicativo. A arquitetura de caneta dá suporte a gestos do sistema e do aplicativo. Há suporte para gestos de aplicativo de traço único e de vários traços.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gestos de aplicativo](application-gestures.md)
</dt> <dt>

[Gestos de movimento](flicks-gestures.md)
</dt> <dt>

[Gestos do sistema](system-gestures.md)
</dt> </dl>

 

 



