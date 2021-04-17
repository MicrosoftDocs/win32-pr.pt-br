---
title: Adicionando o botão de reprodução
description: Adicionando o botão de reprodução
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Criando capas, elemento BUTTONelement
- Aparência do Windows Media Player, elemento BUTTONelement
- elemento skins, BUTTONelement
- arquivos de definição de capa, elemento BUTTONelement
- Elemento BUTTONelement
- elementos, BUTTONelement
- Criando capas, botões de reprodução
- Capas do Windows Media Player, botões de reprodução
- capas, botões de reprodução
- arquivos de definição de capa, botões de reprodução
- Botões de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498710"
---
# <a name="adding-the-play-buttonelement"></a>Adicionando o botão de reprodução

Por fim, você pode adicionar os elementos **buttonelement** que conectam os botões visuais na tela às ações do Windows Media Player. Esse é o núcleo da sua capa e você pode considerá-la como cabeamento da superfície da capa para a maquina interna do Windows Media Player.

O **buttonelement** s está contido em um **Button**. Você deve sempre ter pelo menos um **buttonelement** dentro de cada um dos **botões**.

Coloque o código do **botão** de execução após o colchete angular de fechamento do **botão**.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Os atributos a seguir são usados para definir o **buttonelement** para o botão Play:

**mappingColor**

Esse é o valor de cor de uma região no arquivo de arte de mapeamento que você criou anteriormente. Nesse caso, é a cor verde sólida. Esse atributo é necessário para qualquer **buttonelement**. Ao definir essa cor, você está dizendo ao Windows Media Player para associar essa área de cores ao código XML desse botão.

**upToolTip**

Isso define o texto que será exibido se o usuário passar o mouse sobre o botão. Não confunda isso com a arte de foco que será exibida. Uma dica de ferramenta é uma pequena legenda de balão que leva um tempo para aparecer. No entanto, a imagem de arte em foco será exibida instantaneamente em qualquer cor e forma que você escolher.

**onClick**

Isso define o evento que ocorre quando o mouse clica no botão. O valor desse atributo de evento é chamado de manipulador de eventos e será uma linha de código do Microsoft JScript ou uma função JScript em um arquivo de texto externo que é carregado pelo atributo **loadscript** de uma **exibição**. Nesse caso, o código JScript chama o método de **URL** do Windows Media Player, que carrega e começa a reproduzir um arquivo chamado "Laure. WMA". Observe que a linha termina com um ponto e vírgula dentro das aspas, o que é uma boa prática de codificação JScript. Observe também o uso de aspas simples dentro das aspas duplas para definir o nome do arquivo. Para obter mais informações sobre o JScript, consulte [usando o JScript](using-jscript.md) na seção sobre capas deste SDK.

Observe que não há nenhuma marca **buttonelement** final. Se um elemento não incluir outro elemento, você poderá fechá-lo com a barra invertida logo antes do colchete angular de fechamento. Isso informa ao XML que você terminou com esse elemento. Por exemplo,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



e


```C++
<BUTTONELEMENT/>
```



Transmita as mesmas informações em XML.

O poder das capas vem do uso de manipuladores de eventos. Se o usuário fizer algo com um mouse, você poderá manipular esse evento com o JScript. Seu código pode ser uma única linha que faz com que o Windows Media Player faça algo simples como reproduzir, ou pode ser um aplicativo completo escrito em JScript.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




