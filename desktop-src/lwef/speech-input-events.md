---
title: Eventos de entrada de fala
description: Eventos de entrada de fala
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006188"
---
# <a name="speech-input-events"></a>Eventos de entrada de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Além disso, para a notificação de eventos de [**comando**](command-event.md) , o Agent também notifica o cliente de entrada-ativo quando o servidor ativa ou desativa o modo de escuta, usando os eventos [**ListenStart**](listenstart-event.md) e [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md)). No entanto, se o usuário pressionar a tecla do modo de escuta e não houver nenhum mecanismo de reconhecimento de fala disponível para o caractere superior do cliente de entrada-ativo, o servidor iniciará o tempo limite do modo de teclas de atalho de escuta, mas não gerará um evento **ListenStart** para o cliente ativo do caractere. Se, antes de o tempo limite ser concluído, o usuário ativar outro caractere com suporte ao mecanismo de reconhecimento de fala, o servidor tentará ativar a entrada de fala e gerar o evento **ListenStart** .

Da mesma forma, se um cliente tentar ativar o modo de escuta usando o método [**Listen**](listen-method.md) e não houver nenhum mecanismo de reconhecimento de fala correspondente disponível, a chamada falhará e o servidor não gerará um evento [**ListenStart**](listenstart-event.md). No controle do Microsoft Agent, o método **Listen** retorna **false**, mas a chamada não gera um erro.

Quando o modo de chave de escuta está ativado e o usuário alterna para um caractere que usa um mecanismo de reconhecimento de fala diferente, o servidor alterna para e ativa esse mecanismo e dispara um [**ListenComplete**](listencomplete-event.md) e, em seguida, um evento [**ListenStart**](listenstart-event.md) . Se o caractere ativado não tiver um mecanismo de reconhecimento de fala disponível (porque um não está instalado ou nenhum corresponde à configuração de ID de idioma do caractere ativado), o servidor disparará o evento **ListenComplete** para o caractere anteriormente ativado e retornará um valor no parâmetro de **causa** . No entanto, o servidor não gera eventos **ListenStart** ou **ListenComplete** para os clientes que não têm suporte ao reconhecimento de fala.

Se um cliente chamar com êxito o método [**Listen**](listen-method.md) e um caractere sem o suporte do mecanismo de reconhecimento de fala se tornar a entrada-ativa antes que o tempo limite do modo de escuta seja concluído e, em seguida, o usuário voltar para o caractere do cliente original, o servidor gerará um evento [**ListenStart**](listenstart-event.md) para esse cliente.

Se o cliente de entrada-ativo alternar os mecanismos de reconhecimento de fala alterando [**SRModeID**](srmodeid-property.md) enquanto estiver em modo de escuta, o servidor alternará para e ativará esse mecanismo sem disparar novamente o evento [**ListenStart**](listenstart-event.md) . No entanto, se o mecanismo especificado não estiver disponível, a chamada falhará (gera um erro no controle) e o servidor também chamará o evento [**ListenComplete**](listencomplete-event.md) .

 

 




