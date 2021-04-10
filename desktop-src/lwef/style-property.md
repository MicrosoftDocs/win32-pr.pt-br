---
title: Propriedade de estilo
description: Propriedade de estilo
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292207"
---
# <a name="style-property"></a>Propriedade de estilo

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o estilo de saída do balão de palavras do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres ("*** characterid * * *"). Estilo de balão. estilo* *  \[  =  \]



| Parte    | Descrição                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estilo* | Um inteiro que representa o estilo de saída do balão. A configuração de estilo é um teletexto com bits correspondente a: balão (bit 0), tamanho-para-texto (bit 1), ocultar automaticamente (bit 2), auto-ritmo (bit 3), número de caracteres por linhas (bits 16-23) e número de linhas (bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o bit de estilo de balão é definido como 1, o balão de palavra é exibido quando um método [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Think**](think-method.md) é usado, a menos que o usuário substitua essa configuração na folha de propriedades do Microsoft Agent. Quando definido como 0, um balão não é exibido.

Quando o bit do estilo de tamanho para texto é definido como 1, a palavra balão dimensiona automaticamente a altura do balão para o tamanho atual do texto da instrução [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Think**](think-method.md) . Quando definido como 0, a altura do balão é baseada na configuração da propriedade [**NumberOfLines**](numberoflines-property.md) . Se esse bit de estilo for definido como 1 e você tentar definir a propriedade **NumberOfLines** , o Agent gerará um erro.

Quando o bit de estilo de ocultar automaticamente é definido como 1, o balão de palavras é ocultado automaticamente quando a saída falada é concluída. Quando definido como 0, o balão permanece exibido até a próxima chamada de [**fala**](https://www.bing.com/search?q=**Speak**) ou [**reflexão**](think-method.md) , o caractere é ocultado ou o usuário clica ou arrasta o caractere.

Quando o bit de estilo do ritmo automático é definido como 1, o balão do Word ultrapassa a saída com base na taxa de saída atual, por exemplo, uma palavra de cada vez. Quando a saída excede o tamanho do balão, o texto anterior é rolado automaticamente. Quando definido como 0, todo o texto incluído em uma instrução de [**fala**](https://www.bing.com/search?q=**Speak**) ou [**reflexão**](think-method.md) é exibido ao mesmo tempo.

Para recuperar apenas o valor dos quatro bits inferiores **e** o valor retornado pelo **estilo** com 255. Para definir um valor de bit **ou** o valor retornado com o valor do bits que você deseja definir. Para desativar um bit **e** o valor retornado com um complemento do bit:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



A propriedade **Style** também retorna o número de caracteres por linha no byte inferior da palavra superior e o número de linhas no grande byte da palavra superior. Embora isso possa ser lido com mais facilidade usando as propriedades [**CharsPerLine**](charsperline-property.md) e [**NumberOfLines**](numberoflines-property.md), a propriedade **Style** também permite que você defina esses valores.

Por exemplo, para alterar o número de linhas, desmarque bits 24 para 31 com uma operação **and** lógica antes de definir o novo valor como o produto do novo valor vezes 2 ^ 24, adicionado ao valor existente da propriedade **Style** .


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Para definir o número de caracteres por linha, limpe os bits 16 a 23 com uma operação **and** lógica antes de definir o novo valor como o produto do novo valor vezes 2 ^ 16, adicionado ao valor existente da Propriedade Style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



A propriedade de **estilo** pode ser definida mesmo que o usuário tenha desabilitado a exibição de balão usando a folha de propriedades do Microsoft Agent. No entanto, os valores para o número de linhas devem estar entre 1 e 128 e o número de caracteres por linha deve estar entre 8 e 255. Se você fornecer um valor inválido para a propriedade **Style** , o Agent gerará um erro.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os padrões para esses bits de estilo se baseiam em suas configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

 

 




