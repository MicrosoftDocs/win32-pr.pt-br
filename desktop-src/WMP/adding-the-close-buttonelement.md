---
title: Adicionando o botão fechar
description: Adicionando o botão fechar
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Criando capas, elemento BUTTONelement
- Aparência do Windows Media Player, elemento BUTTONelement
- elemento skins, BUTTONelement
- arquivos de definição de capa, elemento BUTTONelement
- Elemento BUTTONelement
- elementos, BUTTONelement
- Criando capas, botões fechar
- Capas do Windows Media Player, botões fechar
- capas, botões fechar
- arquivos de definição de capa, botões de fechamento
- Botões de fechamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159908"
---
# <a name="adding-the-close-buttonelement"></a>Adicionando o botão fechar

O botão fechar é semelhante em conceito ao botão reproduzir, mas tem códigos e cores diferentes.

Coloque o código do **botão** fecharelement após o colchete angular de fechamento do **botão** de reprodução.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Os atributos a seguir são usados para definir o **buttonelement** para o botão fechar:

**mappingColor**

Esse é o valor de cor da região no arquivo de arte de mapeamento que você criou anteriormente. Nesse caso, é a cor vermelha sólida. Esse atributo é necessário para qualquer **buttonelement**. Ao definir essa cor, você está dizendo ao Windows Media Player para associar essa área de cores ao código XML desse botão.

**upToolTip**

Isso define o texto que será exibido quando o usuário passar o mouse sobre o botão. Isso é o mesmo que o botão Executar, exceto que ele é rotulado como "fechar".

**onClick**

Isso define o evento que ocorre quando o mouse clica no botão. O valor desse atributo de evento é chamado de manipulador de eventos e será uma linha de código do Microsoft JScript ou uma função JScript em um arquivo de texto externo que é carregado pelo atributo **loadscript** de uma **exibição**. Nesse caso, o código JScript chama o método **Close** do elemento **View** usando a **exibição** de atributo global, que fecha a exibição e desliga o Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




