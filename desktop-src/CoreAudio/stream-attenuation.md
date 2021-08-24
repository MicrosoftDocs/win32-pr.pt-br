---
description: Experiência de pato padrão
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiência de pato padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec323bdaf01a7bba0821a9dee2c349239b3a53660334d2ac57edbf71287f396d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695007"
---
# <a name="default-ducking-experience"></a>Experiência de pato padrão

Considere um cenário em que um usuário recebe uma chamada telefônica ao ouvir música no computador. Durante a chamada telefônica, o usuário deseja reduzir o nível de volume da música ao participar da chamada telefônica e retomar o volume original após o término da chamada telefônica. Dependendo das opções especificadas pelo usuário no painel de controle de **sons** , o sistema operacional fornece automaticamente essa funcionalidade por meio da *atenuação* do *pato* ou do fluxo — redução na intensidade de um fluxo de áudio.

A experiência de atenuação padrão depende da preferência do usuário, conforme especificado na opção de **som** do painel de controle. Na guia **comunicações** , o usuário pode escolher um nível de atenuação (o valor padrão é 80%), ativar mudo de todos os fluxos de não comunicação ou desabilitar a experiência de atenuação do fluxo padrão. O sistema permite que novos fluxos de não comunicação (exceto para novos sons do sistema) sejam abertos durante a sessão de comunicação, mas os novos fluxos não são automaticamente atenuados. Quando todos os fluxos de comunicação são fechados, o sistema encerra a sessão de comunicação e restaura o volume dos fluxos que foram atenuados durante a sessão de comunicação.

Para indicar visualmente a atenuação do fluxo, o sistema altera as configurações do mixer de volume dependendo da preferência do usuário. Por exemplo, se o usuário especificar um nível de atenuação, o mixer de volume diminuirá o controle deslizante, exibirá o novo volume atenuado e exibirá o nível de volume original. A imagem a seguir ilustra esse processo.

![diagrama de comportamento de atenuação de fluxo padrão fornecido no Windows 7](images/stream-aatenuation.jpg)

Um aplicativo pode substituir a atenuação de fluxo e implementar uma experiência personalizada de pato se souber quando a sessão de comunicação começa e termina. Para obter mais informações, consulte [fornecendo um comportamento de pato personalizado](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando um dispositivo de comunicação](using-the-communication-device.md)
</dt> <dt>

[Desabilitando a experiência de pato padrão](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornecendo um comportamento personalizado de pato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtendo eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



