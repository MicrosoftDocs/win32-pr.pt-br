---
title: Implementando CPluginWindow
description: Implementando CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-ins do Windows Media Player, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins de interface do usuário, classe CPluginWindow
- Plug-ins de interface do usuário, classe CPluginWindow
- Classe CPluginWindow
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635426"
---
# <a name="implementing-cpluginwindow"></a>Implementando CPluginWindow

A classe CPluginWindow fornece a interface do usuário para o plug-in. No caso do plug-in da interface do usuário de pesquisa, essa classe contém o código para o botão de **pesquisa** e o código que inicia a página de pesquisa quando o botão é clicado.

O assistente fornece uma implementação básica de CPluginWindow no arquivo de cabeçalho CPluginWindow. h. Para manter as coisas simples, o plug-in da interface do usuário de pesquisa modificará esse arquivo diretamente, embora adições extensivas normalmente seriam colocadas em um arquivo CPluginWindow. cpp separado.

As seções a seguir descrevem o que você precisa fazer para implementar o CPluginWindow:

-   [O mapa de mensagens](the-message-map.md)
-   [O Construtor](the-constructor.md)
-   [O método OnPaint](the-onpaint-method.md)
-   [O método OnCreate](the-oncreate-method.md)
-   [O método onsearch](the-onsearch-method.md)
-   [O método LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação de plug-ins de interface do usuário**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




