---
title: IAgentCommands setvoice
description: IAgentCommands setvoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02fb124b51a3be1796258fdcb8ffa31d8b81b59636027f3d99497b27cd2bd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961896"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands:: setvoice

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Define a propriedade de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Um BSTR que especifica o valor para a propriedade de texto de [**voz**](voice-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) deve ter sua propriedade de texto de [**voz**](voice-property.md) definida como acessível por voz. Ele também deve ter sua propriedade [**VoiceCaption**](voicecaption-property.md) ou [**Caption**](caption-property.md) definida para aparecer na janela de comandos de voz e sua propriedade [**Visible**](visible-property.md) definida como **true** para aparecer no menu pop-up do caractere.

A expressão BSTR que você fornece pode incluir caracteres de colchete ( \[ \] ) para indicar palavras opcionais e caracteres de barra vertical ( \| ) para indicar cadeias alternativas. As alternativas devem ser colocadas entre parênteses. Por exemplo, "(Olá \[ \] \| , Oi Olá)" diz ao mecanismo de fala para aceitar "Olá", "Olá", "ou" Olá "para o comando. Lembre-se de incluir os espaços apropriados entre as palavras que você inclui entre colchetes ou parênteses, bem como outro texto. Lembre-se de incluir os espaços apropriados entre o texto entre colchetes ou parênteses e o texto que não está entre colchetes ou parênteses.

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

Portanto, normalmente você deseja usar esses operadores com os caracteres de agrupamento. Por exemplo, a gramática a seguir inclui "Nova York" e "Nova York Nova York":

``` syntax
   "(New York)+"
```

Os operadores de repetição são úteis quando você deseja compor uma gramática que inclui uma sequência repetida, como um número de telefone ou uma especificação de uma lista de itens:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Embora os operadores também possam ser usados com colchetes (um caractere de agrupamento opcional), isso pode reduzir a eficiência do processamento da gramática do agente.

Você também pode usar reticências (...) para dar suporte à chamada de *palavras*, ou seja, dizer ao mecanismo de reconhecimento de fala para ignorar palavras faladas nessa posição na frase (às vezes chamadas de palavras de *lixo* ). Quando você usa reticências, o mecanismo de fala reconhece apenas palavras específicas na cadeia de caracteres, independentemente de quando falado com palavras ou frases adjacentes. Por exemplo, se você definir essa propriedade como " \[ ... \] verificar email \[ ... \] "o mecanismo de reconhecimento de fala corresponderá a frases como" Verifique emails "ou" verificar email "para este comando. As reticências podem ser usadas em qualquer lugar dentro de uma cadeia de caracteres. No entanto, tenha cuidado ao usar essa técnica, já que as configurações de voz com reticências podem aumentar o potencial de correspondências indesejadas.

Ao definir as palavras e a gramática para o comando, inclua pelo menos uma palavra necessária; ou seja, evite fornecer apenas palavras opcionais. Além disso, certifique-se de que a palavra inclua apenas palavras e letras pronunciadas. Para números, é melhor soletrar a palavra em vez de usar uma representação ambígua. Por exemplo, "345" não é um bom formato de gramática. Da mesma forma, em vez de "IEEE", use "I Triple E". Além disso, omita qualquer pontuação ou símbolo. Por exemplo, em vez de " \# $1 10 pizza!", use "o número de 1 10 dólar pizza". Incluir caracteres não pronunciados ou símbolos para um comando pode fazer com que o mecanismo de fala falhe ao compilar a gramática para todos os seus comandos. Por fim, torne seu parâmetro de voz tão distinto como razoavelmente possível de outros comandos de voz que você definir. Quanto maior a similaridade entre a gramática de voz para comandos, mais provável será que o mecanismo de fala faça um erro de reconhecimento. Você também pode usar as pontuações de confiança para distinguir melhor entre dois comandos que podem ter uma gramática de voz semelhante ou semelhante a som.

Você pode incluir em suas palavras-gramáticas na forma de *" \\ pronúncia de texto*", em que "texto" é o texto exibido e "pronúncia" é o texto que esclarece a pronúncia. Por exemplo, a gramática, "1º \\ primeiro", seria reconhecida quando o usuário disser "primeiro", mas o evento [**de comando**](/windows/desktop/lwef/the-command-object) retornará o texto "1º \\ primeiro". Você também pode usar IPA (alfabeto fonético internacional) para especificar uma pronúncia, começando a pronúncia com um caractere de sustenido (" \# ") e o texto que representa a pronúncia IPA.

Para mecanismos de reconhecimento de fala em Japonês, você pode definir a gramática na forma "*kana \\ kanji*", reduzindo as pronúncias alternativas e aumentando a precisão. (A ordenação é revertida para compatibilidade com versões anteriores.) Isso é particularmente importante para a pronúncia de nomes próprios em kanji. No entanto, você pode apenas passar "kanji" sem o kana; nesse caso, o mecanismo deve escutar todas as pronúncias aceitáveis para o kanji. Você também pode passar apenas kana.

Exceto por erros usando os caracteres de formatação de repetição ou agrupamento, o Microsoft Agent não relatará erros na sua gramática, a menos que o mecanismo em si relate o erro. Se você passar o texto na sua gramática de que o mecanismo não consegue compilar, mas o mecanismo não tratar e retornar como erro, o Agent não poderá relatar o erro. Portanto, o aplicativo cliente deve ter cuidado ao definir a gramática para a propriedade de [**voz**](voice-property.md) .

> [!Note]  
> Os recursos de gramática disponíveis podem depender do mecanismo de reconhecimento de fala. Talvez você queira verificar com o fornecedor do mecanismo para determinar quais opções de gramática têm suporte. Use o [**SRModeID**](srmodeid-property.md) para usar um mecanismo específico.

 

A operação dessa propriedade depende do estado do estado de reconhecimento de fala do servidor do Microsoft Agent. Por exemplo, se o reconhecimento de fala estiver desabilitado ou não estiver instalado, essa função não terá efeito imediato. No entanto, se o reconhecimento de fala estiver habilitado durante uma sessão, o comando ficará acessível quando seu aplicativo cliente for de entrada-ativo.

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: getvoice**](iagentcommands--getvoice.md), [**IAgentCommands:: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands:: setVisible**](iagentcommands--setvisible.md)


 

 