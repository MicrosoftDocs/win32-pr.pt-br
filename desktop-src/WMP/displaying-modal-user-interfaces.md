---
title: Exibindo interfaces de usuário modais
description: Exibindo interfaces de usuário modais
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-ins do Windows Media Player, exibindo caixas de diálogo e de mensagens
- plug-ins, exibindo caixas de diálogo e de mensagem
- plug-ins de interface do usuário, exibindo caixas de diálogo e de mensagem
- Plug-ins de interface do usuário, exibindo caixas de diálogo e de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637244"
---
# <a name="displaying-modal-user-interfaces"></a>Exibindo interfaces de usuário modais

Plug-ins de interface do usuário não devem exibir caixas de diálogo modais ou caixas de mensagem em resposta a chamadas de método do Windows Media Player. Por exemplo, não exiba uma caixa de mensagem de sua implementação de **IWMPPluginUI:: Create**.

Se for necessário exibir uma caixa de diálogo ou caixa de mensagem de uma implementação de método de plug-in de interface do usuário chamada pelo Player, você deverá seguir estas etapas:

1.  Registre uma nova mensagem de janela usando **RegisterWindowMessage**.
2.  Envie a mensagem de janela que você registrou para a janela de plug-in da interface do usuário usando a **mensagem de ismessage**.
3.  Mostre a caixa de diálogo ou a caixa de mensagem do manipulador de mensagens para sua nova mensagem de janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do plug-in da interface do usuário**](ui-plug-in-overview.md)
</dt> </dl>

 

 




