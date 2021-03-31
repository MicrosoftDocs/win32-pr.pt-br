---
title: Variáveis para armazenar propriedades
description: Variáveis para armazenar propriedades
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
- Exemplo de plug-in do eco DSP, variáveis para armazenar propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159978"
---
# <a name="variables-to-store-properties"></a>Variáveis para armazenar propriedades

Primeiro, você precisará de uma variável para armazenar o tempo de atraso. O exemplo padrão criado pelo assistente de plug-in do Windows Media Player fornece uma variável chamada m \_ fScaleFactor para armazenar o multiplicador de dimensionamento usado para processamento. Este exemplo não precisa mais dessa variável, portanto, você pode alterar seu nome e tipo para armazenar o valor do tempo de atraso.

1.  Substitua cada instância de m \_ fScaleFactor em Echo. h e Echo. cpp por m \_ dwDelayTime.
2.  Altere o tipo de dados para m \_ fScaleFactor (agora m \_ dwDelayTime) de Double para DWORD em Echo. h.
3.  No construtor para CEcho, altere o valor de tempo de atraso padrão para 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

Em seguida, declare duas novas variáveis de membro para armazenar a porcentagem de sinal de efeito e a porcentagem de sinal de origem a ser misturada no buffer de saída final. O termo "úmida" refere-se ao efeito, e o termo "seca" refere-se ao sinal de origem. Adicione as seguintes declarações a Echo. h:


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Esses valores são armazenados como representações decimais de percentuais para que possam ser facilmente usados como fatores de escala. Por exemplo, uma mistura de 50% de efeito de porcentagem e de 50% de sinal de origem seria representada como um valor de 0,50 para cada variável. A soma dos valores para m \_ fWetMix e m \_ fDryMix não deve ser maior que 1,0 (100 por cento). Eventualmente, esses valores estarão acessíveis como propriedades.

Adicione o seguinte código ao Construtor CEcho para definir os valores padrão como 50% a cada:


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




