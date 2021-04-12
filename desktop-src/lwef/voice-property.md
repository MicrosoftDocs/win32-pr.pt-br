---
title: Propriedade Voice (objeto Commands)
description: Propriedade de voz
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0207fb4fb6f09d460496b6886354bc17738def17
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499205"
---
# <a name="voice-property-commands-object"></a>Propriedade Voice (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o texto que é passado para a gramática do mecanismo de fala (para reconhecimento).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Comandos._ *  \[  =  *cadeia de caracteres* de voz\]



| Parte     | Descrição                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você não fornecer esse parâmetro, o [**VoiceCaption**](voicecaption-property.md) para o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) não aparecerá na janela de comandos de voz.

A expressão de cadeia de caracteres fornecida pode incluir caracteres de colchetes ( \[ \] ) para indicar palavras opcionais e caracteres de barra vertical ( \| ) para indicar cadeias alternativas. As alternativas devem ser colocadas entre parênteses. Por exemplo, "(Olá \[ \] \| , Oi Olá)" diz ao mecanismo de fala para aceitar "Olá", "Olá", "ou" Olá "para o comando. Lembre-se de incluir os espaços apropriados entre o texto entre colchetes ou parênteses e o texto que não está entre colchetes ou parênteses. Você pode usar o operador Star ( \* ) para especificar zero ou mais instâncias das palavras incluídas no grupo ou o operador de adição (+) para especificar uma ou mais instâncias. Por exemplo, os seguintes resultados em uma gramática que dá suporte a "Experimente isto", "Tente isso", "Tente isso", com iterações ilimitadas de "favor":


```
   "please* try this"
```



O seguinte formato de gramática exclui "Experimente isto" porque o operador + define pelo menos uma instância de "por":


```
   "please+ try this"
```



Os operadores de repetição seguem regras normais de precedência e se aplicam ao item de texto imediatamente anterior. Por exemplo, a gramática a seguir resulta em "Nova York" e "Nova York York", mas não em "Nova York Nova York":


```
   "New York+"
```



Portanto, normalmente você deseja usar esses operadores com os caracteres de agrupamento. Por exemplo, a gramática a seguir inclui "Nova York" e "Nova York Nova York":


```
   "(New York)+"
```



Os operadores de repetição são úteis quando você deseja compor uma gramática que inclua uma sequência repetida, como um número de telefone ou uma especificação de uma lista de itens.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Embora os operadores também possam ser usados com o caractere de agrupamento de colchetes opcionais, fazer isso pode reduzir a eficiência do processamento da gramática do agente.

Você também pode usar reticências (...) para dar suporte à chamada de *palavras*, ou seja, dizer ao mecanismo de reconhecimento de fala para ignorar palavras faladas nessa posição na frase (às vezes chamadas de palavras de *lixo* ). Portanto, o mecanismo de fala reconhece apenas palavras específicas na cadeia de caracteres, independentemente de quando falado com palavras ou frases adjacentes. Por exemplo, se você definir essa propriedade como " \[ ... \] verificar email \[ ... \] ", o mecanismo de reconhecimento de fala corresponderá a frases como" verificar email "ou" verificar email "para este comando. As reticências podem ser usadas em qualquer lugar dentro de uma cadeia de caracteres. No entanto, tenha cuidado ao usar essa técnica, pois ela pode aumentar o potencial de correspondências indesejadas.

Ao definir a palavra-gramática para o comando, inclua pelo menos uma palavra necessária; ou seja, evite fornecer apenas palavras opcionais. Além disso, certifique-se de que a palavra inclua apenas palavras e letras pronunciadas. Para números, é melhor soletrar a palavra em vez de usar uma representação ambígua. Por exemplo, "345" não é um bom formato de gramática. Da mesma forma, em vez de "IEEE", use "I Triple E". Além disso, omita qualquer pontuação ou símbolo. Por exemplo, em vez de " \# $1 10 pizza!", use "o número de 1 10 dólar pizza". Incluir caracteres não pronunciados ou símbolos para um comando pode fazer com que o mecanismo de fala falhe ao compilar a gramática para todos os seus comandos. Por fim, torne seu parâmetro de voz tão distinto como razoavelmente possível de outros comandos de voz que você definir. Quanto maior a similaridade entre a gramática de voz para comandos, mais provável será que o mecanismo de fala faça um erro de reconhecimento. Você também pode usar as pontuações de confiança para distinguir melhor entre dois comandos que podem ter uma gramática de voz semelhante ou semelhante a som.

Você pode incluir em suas palavras-gramáticas na forma de *" \\ pronúncia de texto*", em que *texto* é o texto exibido e a *pronúncia* é o texto que esclarece a pronúncia. Por exemplo, a gramática, "1º \\ primeiro", seria reconhecida quando o usuário disser "First", mas o evento de [**comando**](command-event.md) retornará o texto "1º \\ primeiro". Você também pode usar IPA (alfabeto fonético internacional) para especificar uma pronúncia, começando a pronúncia com um caractere de sinal de sustenido (" \# ") e, em seguida, inclua o texto que representa a pronúncia IPA.

Para mecanismos de reconhecimento de fala em Japonês, você pode definir a gramática na forma "*kana \\ kanji*", reduzindo as pronúncias alternativas e aumentando a precisão. (A ordenação é revertida para compatibilidade com versões anteriores.) Isso é particularmente importante para a pronúncia de nomes próprios em kanji. No entanto, você pode apenas passar kanji sem o kana e, nesse caso, o mecanismo deve escutar todas as pronúncias aceitáveis para o kanji. Você também pode passar apenas kana.

Observe também que, para idiomas como japonês, chinês e tailandês, que não usam caracteres de espaço para designar quebras de palavras, insira um caractere de espaço de largura zero (0x200B) Unicode para indicar quebras de palavras lógicas.

Exceto por erros que usam os caracteres de formatação de repetição ou agrupamento, o Agent não relatará erros na sua gramática, a menos que o mecanismo em si relate o erro. Se você passar o texto na sua gramática de que o mecanismo não consegue compilar, mas o mecanismo não tratar e retornar como erro, o Agent não poderá relatar o erro. Portanto, o aplicativo cliente deve ser definir cuidadosamente a gramática para a propriedade de **voz** .

> [!Note]  
> Os recursos de gramática disponíveis podem depender do mecanismo de reconhecimento de fala. Talvez você queira verificar com o fornecedor do mecanismo para determinar quais opções de gramática têm suporte. Use o [**SRModeID**](srmodeid-property.md) para usar um mecanismo específico.

 

A operação dessa propriedade depende do estado da propriedade de reconhecimento de fala do servidor. Por exemplo, se o reconhecimento de fala estiver desabilitado ou não estiver instalado, essa propriedade não terá nenhum efeito.

 

 
