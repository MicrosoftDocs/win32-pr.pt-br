---
title: Adicionando o botão fechar
description: Adicionando o botão fechar
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Criando capas, elemento BUTTONelement
- Windows Media Player skins, elemento buttonelement
- elemento skins, BUTTONelement
- arquivos de definição de capa, elemento BUTTONelement
- Elemento BUTTONelement
- elementos, BUTTONelement
- Criando capas, botões fechar
- Windows Media Player aparências, botões fechar
- capas, botões fechar
- arquivos de definição de capa, botões de fechamento
- Botões de fechamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765467"
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

Esse é o valor de cor da região no arquivo de arte de mapeamento que você criou anteriormente. Nesse caso, é a cor vermelha sólida. Esse atributo é necessário para qualquer **buttonelement**. ao definir essa cor, você está dizendo Windows Media Player para associar essa área de cores ao código XML desse botão.

**upToolTip**

Isso define o texto que será exibido quando o usuário passar o mouse sobre o botão. Isso é o mesmo que o botão Executar, exceto que ele é rotulado como "fechar".

**onClick**

Isso define o evento que ocorre quando o mouse clica no botão. o valor desse atributo de evento é chamado de manipulador de eventos e será uma linha do código de JScript da Microsoft ou uma função JScript em um arquivo de texto externo que é carregado pelo atributo **loadscript** de uma **exibição**. nesse caso, o código de JScript chama o método **close** do elemento **VIEW** usando a **exibição** de atributo global, que fecha a exibição e desliga Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




