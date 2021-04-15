---
title: Arquivo de definição de capa
description: Arquivo de definição de capa
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761280"
---
# <a name="skin-definition-file"></a>Arquivo de definição de capa

Os arquivos de definição de capa contêm as instruções básicas para o que a capa faz e onde outros arquivos usados pela capa podem ser encontrados. Só pode haver um arquivo de definição de capa para uma capa e ele tem uma extensão de nome de arquivo. WMS.

As instruções no arquivo de definição de capa são escritas em linguagem XML (XML), que é semelhante ao HTML. Se você tiver usado HTML para criar páginas da Web, verá que o XML parece familiar.

O XML no arquivo de definição de capa usa um conjunto de marcas de elemento especiais para definir partes da interface do usuário de capa. Por exemplo, o elemento [Button](button-element.md) define como um botão se comportará, onde ele vai e como será a aparência.

Cada marca de elemento tem atributos específicos. Por exemplo, o elemento [Button](button-element.md) tem um atributo **Image** que define onde a imagem do botão pode ser encontrada. Isso é semelhante ao HTML, onde o elemento BODY terá um atributo **bgcolor** que define a cor do plano de fundo da página HTML. Informações detalhadas sobre todos os elementos de capa e seus atributos estão incluídas na seção de [referência de programação de capa](skin-programming-reference.md) .

O XML tem algumas regras simples que você precisa saber para criar capas. Ao contrário do HTML, o XML exige que você siga as regras exatamente.

## <a name="enclose-elements-with-angle-brackets"></a>Incluir elementos com colchetes angulares

Todos os elementos são colocados entre colchetes angulares; por exemplo, o elemento **Button** é digitado da seguinte maneira:


```C++
<BUTTON>

```



Você não precisa digitar a palavra "BUTTON" em letras maiúsculas, mas a Convenção de digitação de nomes de elementos em letras maiúsculas é usada no código de exemplo desse SDK.

## <a name="put-attributes-before-the-closing-bracket"></a>Colocar atributos antes do colchete de fechamento

Todos os atributos de um determinado elemento devem ser incluídos antes do colchete angular de fechamento. Um atributo consiste no nome do atributo seguido por um sinal de igual (=) e o valor do atributo entre aspas.


```C++
<BUTTON image="mypic.jpg">

```



Não é necessário digitar a palavra "Image" em minúsculas, mas a Convenção de digitação de nomes de atributo em minúsculas é usada no código de exemplo desse SDK. Observe também que o valor do atributo é colocado entre aspas.

## <a name="opening-and-closing-elements"></a>Elementos de abertura e fechamento

Alguns elementos são agrupados dentro de outro elemento. Por exemplo, o elemento de **botão** não faz muito sentido, a menos que você use um ou mais elementos **buttonelement** com ele. Para tornar o agrupamento claro, você precisa ter uma marca de abertura e de fechamento para cada elemento. A marca de abertura é apenas o nome do elemento e quaisquer atributos relacionados, entre colchetes angulares. A marca de fechamento é o nome do elemento, precedido por uma barra (/) e, em seguida, entre colchetes angulares. Por exemplo, a marca de abertura do elemento do tipo de **botão** tem esta aparência:


```C++
<BUTTONGROUP>

```



A marca do bloco de **botões** de fechamento tem esta aparência:


```C++
</BUTTONGROUP>

```



Você colocaria as marcas **buttonelement** entre as marcas de elemento do **botão** de abertura e de fechamento. Por exemplo:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Fechando elementos

Se um elemento não tiver outros elementos dentro dele, você deverá colocar uma barra no final do nome do elemento logo antes do colchete angular de fechamento. Por exemplo, no código acima, cada elemento **buttonelement** tem uma barra "/" para indicar que não há outros elementos aninhados dentro dele.

Em outras palavras, você deve ter uma marca de elemento de fechamento ou fechar seu elemento com uma barra.

Isso está correto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Isso não está correto:


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Isso também não está correto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



A seção a seguir fornece mais informações sobre arquivos de definição de capa:

-   [Estrutura do arquivo de definição de capa](skin-definition-file-structure.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de capa**](skin-files.md)
</dt> </dl>

 

 




