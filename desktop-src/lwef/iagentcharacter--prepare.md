---
title: IAgentCharacter preparar
description: IAgentCharacter preparar
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de29c49960bbfd00a6e0d0e9ff1cb055a01cb930c414708fe9144ff0ff4b75af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725309"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P reparênteses

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Recupera dados de animação para um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Um valor que indica o tipo de dados de animação a ser carregado que deve ser um dos seguintes:



| Valor                                                           | Descrição                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| animação de **curta preparação não assinada const** **\_ = 0;**<br/> | Dados de animação de um caractere.                              |
| **const estado curto de preparação não assinado** **\_ = 1;**<br/>     | Dados de estado de um caractere.                                  |
| **const de curto-circuito sem sinal constante** **\_ = 2**<br/>       | Um arquivo de som de um caractere (. WAV ou. LWV) para saída falada. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

O nome da animação ou do estado.

O nome da animação é baseado nessa definição para o caractere quando ele foi salvo usando o editor de caracteres do Microsoft Agent.

Para Estados, o valor pode ser um dos seguintes:



|                      | Descrição                                     |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | Para recuperar todas as animações de estado **gesturing** . |
| **"GesturingDown"**  | Para recuperar animações **GesturingDown** .       |
| **"GesturingLeft"**  | Para recuperar animações **GesturingLeft** .       |
| **"GesturingRight"** | Para recuperar animações **GesturingRight** .      |
| **"GesturingUp"**    | Para recuperar animações **GesturingUp** .         |
| **Ocultar**         | Para recuperar as animações de estado **ocultos** .    |
| **Auditiva**        | Para recuperar as animações de estado **audição** .   |
| **Deixar**         | Para recuperar todas as animações de estado **deixar** .    |
| **"IdlingLevel1"**   | Para recuperar todas as animações **IdlingLevel1** .    |
| **"IdlingLevel2"**   | Para recuperar todas as animações **IdlingLevel2** .    |
| **"IdlingLevel3"**   | Para recuperar todas as animações **IdlingLevel3** .    |
| **Detecta**      | Para recuperar as animações do estado de **escuta** . |
| **Movimenta**         | Para recuperar todas as animações de estado **móvel** .    |
| **"MovingDown"**     | Para recuperar todas as animações em **movimento** .          |
| **"MovingLeft"**     | Para recuperar todas as animações **MovingLeft** .      |
| **"MovingRight"**    | Para recuperar todas as animações **MovingRight** .     |
| **"MovingUp"**       | Para recuperar todas as animações **MovingUp** .        |
| **Mostrando**        | Para recuperar as animações de estado em **exibição** .   |
| **Língua**       | Para recuperar as animações de estado de **fala** .  |



 

Fins. Arquivos WAV, defina *bszName* para a especificação de URL ou arquivo para o. Arquivo WAV. Se a especificação não for concluída, ela será interpretada como sendo relativa à especificação usada no método [**Load**](https://www.bing.com/search?q=**Load**) .

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Um booliano que especifica se o servidor enfileira a solicitação de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) . **True** enfileira a solicitação e faz com que qualquer solicitação de animação a seguir aguarde até que os dados de animação que ele especifica sejam carregados. **False** recupera os dados de animação de forma assíncrona.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) .

</dd> </dl>

Se você carregar um caractere usando o protocolo HTTP (um. Arquivo ACF), você deve usar o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar dados de animação antes de poder reproduzir a animação. Você não poderá usar esse método se tiver carregado o caractere usando o protocolo UNC (um. Arquivo ACS). Você também não pode recuperar dados HTTP para um caractere usando **Prepare** se você carregou esse caractere usando o protocolo UNC (. Arquivo de caracteres do ACS).

Dados de animação ou de som recuperados com o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) são armazenados no cache do navegador. As chamadas subsequentes verificarão o cache e, se os dados da animação já estiverem lá, o controle carregará os dados diretamente do cache. Depois de carregados, os dados de animação ou de som podem ser reproduzidos com os métodos [**Play**](/windows/desktop/lwef/iagentcharacter--play) ou [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

Você pode especificar várias animações e Estados separando-os com vírgulas. No entanto, você não pode misturar tipos na mesma instrução [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .

 

