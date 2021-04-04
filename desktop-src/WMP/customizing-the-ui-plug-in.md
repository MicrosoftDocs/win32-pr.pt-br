---
title: Personalizando o plug-in da interface do usuário
description: Personalizando o plug-in da interface do usuário
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-ins do Windows Media Player, personalizando
- plug-ins, personalizando
- plug-ins de interface do usuário, personalizando
- Plug-ins de interface do usuário, personalizando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005927"
---
# <a name="customizing-the-ui-plug-in"></a>Personalizando o plug-in da interface do usuário

Neste ponto, seu projeto está pronto para personalização. Você pode modificar a implementação gerada pelo assistente da interface **IWMPPluginUI** , pode adicionar uma interface do usuário à classe **CPluginWindow** , e você pode implementar uma página de propriedades na classe **CPropertyDialog** . Se o seu plug-in estiver configurado para escutar eventos do Windows Media Player, o assistente terá gerado implementações padrão ou vazias de todos os manipuladores de eventos necessários, que você também modificará ou criará.

O tipo de plug-in e os recursos aos quais ele dá suporte são indicados por um valor que é armazenado no registro do Windows. O assistente gera um arquivo com uma extensão de nome de arquivo. rgs que contém as informações para registrar o plug-in com o. O valor de "recursos" nesse arquivo é o equivalente Decimal de um booliano ou das constantes de tipo de plug-in e dos sinalizadores de plug-in definidos em wmpplug. h. Embora esse valor seja determinado pelas opções selecionadas no assistente, você deve modificá-lo se desejar criar um plug-in com várias predefinições ou uma para a qual os itens de mídia ou listas de reprodução possam ser enviadas.

Conforme você modifica e estende seu código de plug-in, você pode criar e registrar sua DLL para que possa testar seu plug-in no Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um plug-in de interface do usuário**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




