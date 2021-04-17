---
title: IAgentCommand setvoice
description: IAgentCommand setvoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105782662"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand:: setvoice

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Define a propriedade de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Um BSTR que especifica o texto para a propriedade de [**voz**](voice-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade de [**voz**](voice-property.md) e a propriedade [**habilitada**](enabled-property.md) definida como sendo acessível por voz. Ele também deve ter sua propriedade [**VoiceCaption**](voicecaption-property.md) definida para aparecer na **janela de comandos de voz**. (Para compatibilidade com versões anteriores, se não houver nenhum **VoiceCaption**, a configuração de [**legenda**](caption-property.md) será usada.)

A expressão BSTR que você fornece pode incluir caracteres de colchete ( \[ \] ) para indicar palavras opcionais e caracteres de barra vertical ( \| ) para indicar cadeias alternativas. As alternativas devem ser colocadas entre parênteses. Por exemplo, "(Olá \[ \] \| , Oi Olá)" diz ao mecanismo de fala para aceitar "Olá", "Olá", "ou" Olá "para o comando. Lembre-se de incluir os espaços apropriados entre o texto entre colchetes ou parênteses e o texto que não está entre colchetes ou parênteses.

Você pode usar o operador Star ( \* ) para especificar zero ou mais instâncias das palavras incluídas no grupo ou o operador de adição (+) para especificar uma ou mais instâncias. Por exemplo, os seguintes resultados em uma gramática que dá suporte a "Experimente isto", "Tente isso" e "Tente isso", com iterações ilimitadas de "favor":

``` syntax
   "please* try this"
```

O seguinte formato de gramática exclui "Experimente isto" porque o operador + define pelo menos uma instância de "por":

``` syntax
   "please+ try this"
```

Os operadores de repetição seguem regras normais de precedência e se aplicam ao item de texto imediatamente anterior. Por exemplo, a gramática a seguir resulta em "Nova York" e "Nova York York", mas não em "Nova York Nova York":

``` syntax
   "New York+"
```

Portanto, normalmente você desejará usar esses operadores com os caracteres de agrupamento. Por exemplo, a gramática a seguir inclui "Nova York" e "Nova York Nova York":

``` syntax
   "(New York)+"
```

Os operadores de repetição são úteis quando você deseja compor uma gramática que inclui uma sequência repetida, como um número de telefone ou uma especificação de uma lista de itens:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Embora os operadores também possam ser usados com colchetes (um caractere de agrupamento opcional), isso pode reduzir a eficiência do processamento da gramática do agente.

Você também pode usar reticências (...) para dar suporte à chamada de *palavras*, ou seja, dizer ao mecanismo de reconhecimento de fala para ignorar palavras faladas nessa posição na frase (às vezes chamadas de palavras de *lixo* ). Portanto, o mecanismo de fala reconhece apenas palavras específicas na cadeia de caracteres, independentemente de quando falado com palavras ou frases adjacentes. Por exemplo, se você definir essa propriedade como " \[ ... \] verificar email \[ ... \] "o mecanismo de reconhecimento de fala corresponderá a frases como" Verifique emails "ou" verificar email "para este comando. As reticências podem ser usadas em qualquer lugar dentro de uma cadeia de caracteres. No entanto, tenha cuidado ao usar essa técnica, pois as configurações de voz com reticências podem aumentar o potencial de correspondências indesejadas.

Ao definir as palavras e a gramática para o comando, sempre certifique-se de incluir pelo menos uma palavra necessária; ou seja, evite fornecer apenas palavras opcionais. Além disso, certifique-se de que a palavra inclua apenas palavras e letras pronunciadas. Para números, é melhor soletrar a palavra em vez de usar a representação numérica. Além disso, omita qualquer pontuação ou símbolo. Por exemplo, em vez de " \# $1 10 pizza!", use "o número de 1 10 dólar pizza". Incluir caracteres não pronunciados ou símbolos para um comando pode fazer com que o mecanismo de fala falhe ao compilar a gramática para todos os seus comandos. Por fim, torne seu parâmetro de voz tão distinto como razoavelmente possível de outros comandos de voz que você definir. Quanto maior a similaridade entre a gramática de voz para comandos, mais provável será que o mecanismo de fala faça um erro de reconhecimento. Você também pode usar as pontuações de confiança para distinguir melhor entre dois comandos que podem ter uma gramática de voz semelhante ou semelhante a som.

Definir a propriedade de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) habilita automaticamente os serviços de fala do agente, disponibilizando a chave de escuta e a dica de escuta disponíveis. No entanto, ele não carrega o mecanismo de reconhecimento de fala.

> [!Note]  
> Os recursos de gramática disponíveis podem depender do mecanismo de reconhecimento de fala. Talvez você queira verificar com o fornecedor do mecanismo para determinar quais opções de gramática têm suporte. Use [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) para especificar um mecanismo.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: getvoice**](iagentcommand--getvoice.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setativated**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 