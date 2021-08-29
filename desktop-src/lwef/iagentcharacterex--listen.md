---
title: IAgentCharacterEx Listen
description: IAgentCharacterEx Listen
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee221de03fe0a0e908e1fc3c10f05d48c26dd9fd264edd20ee2e4d78d73fb91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105494"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx::Listen

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Ativa ou desliga o modo de escuta (entrada de reconhecimento de fala).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Sinalizador de modo de escuta. Se esse parâmetro for **True,** o modo de escuta será ligado; se **False**, o modo de escuta será desligado.

</dd> </dl>

Definir esse método como **True** habilita o modo de Escuta (ativa o reconhecimento de fala) por um período fixo. Embora não seja possível definir o valor do tempo-expirado, você pode desativar o modo de escuta antes que o tempo-expirar. Além disso, se o modo de escuta já estiver ativa porque você (ou outro cliente) definiu com êxito o método como **True** antes que o tempo-expirar, o método terá êxito e redefinirá o tempo-expirado. No entanto, se o modo de Escuta já estiver ativa porque o usuário está pressionando a tecla Listening, o método será bem-sucedido, mas o tempo-tempo será ignorado e o modo de escuta terminará com base na interação do usuário com a tecla Listening.

Esse método terá êxito somente quando chamado pelo cliente input-active. Portanto, o método falhará se o cliente não for o cliente ativo do caractere mais alto. O método também falhará se você tentar definir o método como **False** e o usuário estiver pressionando a tecla Listening. Ele também poderá falhar se não houver nenhum mecanismo de fala compatível disponível que corresponde à configuração de ID de idioma do caractere ou se o usuário tiver desabilitado a entrada de fala usando a folha de propriedades do Microsoft Agent. No entanto, o método não falhará se o dispositivo de áudio estiver ocupado.

Quando você definiu esse método com êxito como **True**, o servidor dispara o [**evento IAgentNotifySinkEx::ListeningState.**](iagentnotifysinkex--listeningstate.md) O servidor também envia **IAgentNotifySinkEx::ListeningState** quando o tempo-out do modo de escuta for concluído ou quando você definir [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.

Esse método não chama [**automaticamente IAgentCharacter::StopAll**](iagentcharacter--stopall.md) e reproduz uma animação de estado de escuta do caractere, como ocorre quando o usuário pressiona a tecla Listening. Isso permite que você use o evento [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) para determinar se deseja interromper a animação atual e reproduzir sua própria animação apropriada. No entanto, depois que um enunciado de usuário é detectado, o servidor chama **automaticamente IAgentCharacter::StopAll** e reproduz uma animação de estado auditivo.

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




