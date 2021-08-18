---
title: Exibindo interfaces de usuário modais
description: Exibindo interfaces de usuário modais
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player plug-ins, exibindo caixas de diálogo e mensagem
- plug-ins, exibindo caixas de diálogo e mensagem
- plug-ins de interface do usuário, exibindo caixas de diálogo e mensagem
- Plug-ins de interface do usuário, exibindo caixas de diálogo e mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addacfe2a309808f949c59a8ec11498417cb05a17cd6ab160ca1c08d2017a0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997236"
---
# <a name="displaying-modal-user-interfaces"></a>Exibindo interfaces de usuário modais

Os plug-ins de interface do usuário não devem exibir caixas de diálogo modais ou caixas de mensagem em resposta a chamadas de método de Windows Media Player. Por exemplo, não ex exibir uma caixa de mensagem de sua implementação **de IWMPPluginUI::Create**.

Se você deve exibir uma caixa de diálogo ou uma caixa de mensagem de uma implementação de método de plug-in de interface do usuário chamada pelo Player, siga estas etapas:

1.  Registre uma nova mensagem de janela **usando RegisterWindowMessage**.
2.  Envie a mensagem de janela que você registrou para a janela de plug-in da interface do usuário usando **o PostMessage**.
3.  Mostre a caixa de diálogo ou a caixa de mensagem do manipulador de mensagens para a nova mensagem de janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do plug-in da interface do usuário**](ui-plug-in-overview.md)
</dt> </dl>

 

 




