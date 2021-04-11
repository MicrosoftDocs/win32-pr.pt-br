---
title: Escuta IAgentCharacterEx
description: Escuta IAgentCharacterEx
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292363"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx:: escutar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Ativa ou desativa o modo de escuta (entrada de reconhecimento de fala).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Sinalizador de modo de escuta. Se esse parâmetro for **true**, o modo de escuta será ativado; Se for **false**, o modo de escuta será desativado.

</dd> </dl>

Definir esse método como **true** habilita o modo de escuta (ativa o reconhecimento de fala) por um período de tempo fixo. Embora não seja possível definir o valor do tempo limite, você pode desligar o modo de escuta antes que o tempo limite expire. Além disso, se o modo de escuta já estiver ativo porque você (ou outro cliente) definiu com êxito o método como **verdadeiro** antes de expirar o tempo limite, o método terá êxito e redefinirá o tempo limite. No entanto, se o modo de escuta já estiver ativado porque o usuário está pressionando a tecla de escuta, o método terá sucesso, mas o tempo limite será ignorado e o modo de escuta terminará com base na interação do usuário com a chave de escuta.

Esse método terá sucesso somente quando chamado pelo cliente de entrada-ativo. Portanto, o método falhará se o cliente não for o cliente ativo do caractere superior. O método também falhará se você tentar definir o método como **false** e o usuário estiver pressionando a tecla de escuta. Ele também pode falhar se não houver nenhum mecanismo de fala compatível disponível que corresponda à configuração de ID de idioma do caractere ou o usuário tenha desabilitado a entrada de fala usando a folha de propriedades do Microsoft Agent. No entanto, o método não falhará se o dispositivo de áudio estiver ocupado.

Quando você define com êxito esse método como **true**, o servidor dispara o evento [**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md) . O servidor também envia **IAgentNotifySinkEx:: listeningstate** quando o tempo limite do modo de escuta é concluído ou quando você define [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) como **false**.

Esse método não chama automaticamente [**IAgentCharacter:: Enopall**](iagentcharacter--stopall.md) e executa uma animação de estado de escuta do caractere, como ocorre quando o usuário pressiona a tecla de escuta. Isso permite que você use o evento [**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md) para determinar se deseja parar a animação atual e executar sua própria animação apropriada. No entanto, quando um usuário expressão é detectado, o servidor chama automaticamente **IAgentCharacter:: Adopall** e desempenha uma animação de estado audição.

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySinkEx:: listeningstate**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: getabilited**](iagentspeechinputproperties--getenabled.md)


 

 




