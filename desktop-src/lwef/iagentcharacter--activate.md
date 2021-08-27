---
title: IAgentCharacter Activate
description: IAgentCharacter Activate
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7256b1d155b051985c72120283e60896026218ea81d8b2b9c37dc94fb52bb63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750992"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter::Activate

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Define se um cliente está ativo ou se um caractere é mais alto.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retorna S \_ FALSE para indicar que a operação não foi bem-sucedida.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Você pode especificar os seguintes valores para este parâmetro:



| Valor | Descrição                   |
|-------|-------------------------------|
| 0     | De definido como não o cliente ativo. |
| 1     | Definido como o cliente ativo.     |
| 2     | Faça o caractere mais alto.   |



 

</dd> </dl>

Quando vários caracteres estão visíveis, apenas um dos caracteres recebe entrada de fala por vez. Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, apenas um dos clientes recebe entrada do mouse (por exemplo, eventos de clique ou arrastar do controle do Microsoft Agent) por vez. O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere mais alto e o cliente que recebe a entrada é o cliente ativo do caractere. (A janela do caractere superior também aparece na parte superior da ordem z da janela de caracteres.) Normalmente, o usuário determina qual caractere é mais alto selecionando-o explicitamente. No entanto, a ativação mais alta também muda quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais superior, respectivamente.)

Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe entradas direcionadas para o caractere, como quando o próprio aplicativo se torna ativo. Por exemplo, definir **Estado** como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere. Portanto, ele também torna seu cliente o cliente ativo de entrada do caractere. No entanto, você também pode definir o cliente ativo para um caractere sem tornar o caractere mais alto, definindo **Estado** como 1. Isso permite que o cliente receba uma entrada direcionada para esse caractere quando o caractere se torna mais alto. Da mesma forma, você pode definir seu cliente como não ser o cliente ativo (para não receber entrada) quando o caractere se torna mais alto, definindo **Estado** como 0. Você pode determinar se um caractere tem outros clientes atuais usando [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).

Evite chamar esse método diretamente após um [**método**](iagentcharacter--show.md) Show. **Mostrar** define automaticamente o cliente ativo de entrada. Quando o caractere estiver oculto, **a chamada Ativar** poderá falhar se for processada antes da conclusão **do** método Show.

A tentativa de chamar esse método com **o parâmetro State** definido como 2 (quando o caractere especificado está oculto) falhará. Da mesma forma, se você definir **Estado** como 0 e seu aplicativo for o único cliente, essa chamada falhará. Um caractere sempre deve ter um cliente mais alto.

> [!Note]  
> Chamar esse método com **State** definido como 1 normalmente não gera um [**evento AgentNotifySink::ActivateInputState,**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a menos que não haja outros caracteres carregados ou seu aplicativo já esteja ativo de entrada.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




