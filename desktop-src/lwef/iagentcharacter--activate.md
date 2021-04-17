---
title: IAgentCharacter ativar
description: IAgentCharacter ativar
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498822"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter:: ativar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Define se um cliente está ativo ou se um caractere está no nível mais alto.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retorna S \_ false para indicar que a operação não foi bem-sucedida.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Você pode especificar os seguintes valores para este parâmetro:



| Valor | Descrição                   |
|-------|-------------------------------|
| 0     | Defina como não o cliente ativo. |
| 1     | Defina como o cliente ativo.     |
| 2     | Faça o caractere superior.   |



 

</dd> </dl>

Quando vários caracteres são visíveis, apenas um dos caracteres recebe a entrada de fala de cada vez. Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, apenas um dos clientes recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos) de cada vez. O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere superior e o cliente que recebe a entrada é o cliente ativo do caractere. (A janela do caractere superior também aparece na parte superior da ordem z da janela de caractere.) Normalmente, o usuário determina qual caractere é mais alto selecionando-o explicitamente. No entanto, a ativação na extremidade superior também é alterada quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais o mais alto, respectivamente.)

Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe a entrada direcionada para o caractere, como quando o próprio aplicativo se torna ativo. Por exemplo, definir **State** como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere. Portanto, ele também torna o cliente o cliente de entrada-ativo do caractere. No entanto, você também pode definir o cliente ativo para um caractere sem tornar o caractere mais alto, definindo o **estado** como 1. Isso permite que o cliente receba entrada direcionada para esse caractere quando o caractere se tornar mais alto. Da mesma forma, você pode definir que o cliente não seja o cliente ativo (para não receber a entrada) quando o caractere se tornar mais alto, definindo **State** como 0. Você pode determinar se um caractere tem outros clientes atuais usando [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).

Evite chamar esse método diretamente após um método [**show**](iagentcharacter--show.md) . **Mostrar** define automaticamente o cliente de entrada-ativo. Quando o caractere estiver oculto, a chamada **Ativar** poderá falhar, se for processada antes que o método **show** seja concluído.

A tentativa de chamar esse método com o parâmetro de **estado** definido como 2 (quando o caractere especificado estiver oculto) falhará. Da mesma forma, se você definir **State** como 0 e seu aplicativo for o único cliente, essa chamada falhará. Um caractere sempre deve ter um cliente superior.

> [!Note]  
> Chamar esse método com o **estado** definido como 1 normalmente não gera um evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) , a menos que não haja nenhum outro caractere carregado ou que seu aplicativo já esteja em entrada-ativo.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




