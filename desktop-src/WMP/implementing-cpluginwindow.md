---
title: Implementando CPluginWindow
description: Implementando CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player plug-ins, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins de interface do usuário, classe CPluginWindow
- Plug-ins de interface do usuário, classe CPluginWindow
- Classe CPluginWindow
- guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748131"
---
# <a name="implementing-cpluginwindow"></a>Implementando CPluginWindow

A classe CPluginWindow fornece a interface do usuário para o plug-in. No caso do plug-in pesquisar interface do usuário,  essa classe contém o código para o botão Pesquisar e o código que inicia a página de pesquisa quando o botão é clicado.

O assistente fornece uma implementação básica de CPluginWindow no arquivo de header CPluginWindow.h. Para manter as coisas simples, o plug-in pesquisar interface do usuário modificará esse arquivo diretamente, embora extensivas adições normalmente seriam colocadas em um arquivo CPluginWindow.cpp separado.

As seções a seguir descrevem o que você precisa fazer para implementar o CPluginWindow:

-   [O mapa de mensagens](the-message-map.md)
-   [O construtor](the-constructor.md)
-   [O método OnPaint](the-onpaint-method.md)
-   [O método OnCreate](the-oncreate-method.md)
-   [O método OnSearch](the-onsearch-method.md)
-   [O método LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface do Usuário guia de programação de plug-ins**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




