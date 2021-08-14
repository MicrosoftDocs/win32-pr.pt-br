---
title: Adicionando o BOTÃO DE ReproduçãoELEMENT
description: Adicionando o BOTÃO DE ReproduçãoELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- criando capas, elemento BUTTONELEMENT
- Windows Media Player capas, elemento BUTTONELEMENT
- skins, elemento BUTTONELEMENT
- arquivos de definição de capa, elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elements,BUTTONELEMENT
- criando capas, botões reproduzir
- Windows Media Player capas, botões reproduzir
- capas, botões reproduzir
- arquivos de definição de capa, botões Reproduzir
- Botões de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab52691b48876327f45fbaf30a98de78c8c0c46a2eafd0a2c342e51c5a8683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583540"
---
# <a name="adding-the-play-buttonelement"></a>Adicionando o BOTÃO DE ReproduçãoELEMENT

Por fim, você pode adicionar os **elementos BUTTONELEMENT** que conectam os botões visuais na tela para Windows Media Player ações. Esse é o núcleo da sua capa e você pode pensar nele como a conexão da superfície da capa à máquina interna de Windows Media Player.

**BUTTONELEMENT** s estão contidos em um **BUTTONGROUP.** Você sempre deve ter pelo menos um **BUTTONELEMENT dentro** de cada **BUTTONGROUP.**

Coloque o código **BUTTONELEMENT de** Reprodução após o colchete angular de fechamento **de BUTTONGROUP.**


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Os seguintes atributos são usados para definir **o BUTTONELEMENT** para o botão Reproduzir:

**Mappingcolor**

Esse é o valor de cor de uma região no arquivo de arte de mapeamento que você criou antes. Nesse caso, é a cor verde sólida. Esse atributo é necessário para qualquer **BUTTONELEMENT.** Ao definir essa cor, você está Windows Media Player associar essa área de cor ao código XML desse botão.

**upToolTip**

Isso define o texto que será exibido se o usuário passar o mouse sobre o botão. Não confunda isso com a arte de foco que será exibida. Uma Dica de Ferramenta é uma pequena legenda de balão que leva um tempo para aparecer. No entanto, a imagem de arte de foco aparecerá instantaneamente em qualquer cor e forma escolhidas.

**Onclick**

Isso define o evento que ocorre quando o mouse clica no botão. O valor desse atributo de evento é chamado de manipulador de eventos e será uma linha de código do Microsoft JScript ou uma função JScript em um arquivo de texto externo carregado pelo atributo **loadScript** de um **VIEW**. Nesse caso, o código JScript chama o método **url** de Windows Media Player, que carrega e começa a tocar um arquivo chamado "laure.wma". Observe que a linha termina com um ponto e vírgula dentro das aspas, o que é uma boa JScript de codificação. Observe também o uso de aspas simples dentro das aspas duplas para definir o nome do arquivo. Para obter mais informações JScript, consulte [Usando JScript](using-jscript.md) na seção Sobre capas deste SDK.

Observe que não há nenhuma marca **BUTTONELEMENT** final. Se um elemento não incluir outro elemento, você poderá fechar com a barra para frente logo antes do colchete angular de fechamento. Isso informa ao XML que você terminou com esse elemento. Por exemplo,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



e


```C++
<BUTTONELEMENT/>
```



transmitem as mesmas informações em XML.

O poder das capas vem do uso de manipuladores de eventos. Se o usuário fizer algo com um mouse, você poderá manipular esse evento com JScript. Seu código pode ser uma única linha que Windows Media Player fazer algo simples como reproduzir ou pode ser um aplicativo completo escrito em JScript.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




