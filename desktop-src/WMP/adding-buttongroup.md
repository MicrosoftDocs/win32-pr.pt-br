---
title: Adicionando um botão
description: Adicionando um botão
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Criando capas, elemento de botão
- Windows Media Player capas, elemento de botão
- capas, elemento de botão
- arquivos de definição de capa, elemento de botão
- Elemento de botão
- elementos, um botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865184"
---
# <a name="adding-buttongroup"></a>Adicionando um botão

Este exemplo usa o elemento de grupo de **botões** para a codificação no arquivo de definição de capa. O tipo de **botão** cria uma maneira fácil de processar eventos de mouse sem a necessidade de calcular os locais exatos na tela e usa a cor em vez das coordenadas x e y.

Primeiro, você deve adicionar as marcas de grupo de **botões** ao arquivo de definição de capa que você criou. Coloque-os após os atributos de marca de **tema** .


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Deixe algumas linhas em branco acima da marca do **botão** de fechamento para os botões que serão adicionados a seguir.

Os seguintes atributos são usados para definir o **botão**:

**mappingImage**

Esse é o nome de arquivo do arquivo de arte de mapeamento criado anteriormente, aquele com os círculos vermelho e verde. Esse atributo é necessário para qualquer um dos **botões**.

**hoverImage**

Esse é o nome do arquivo Art que você criou anteriormente, aquele com os dois botões amarelos que lêem "Play" e "Close". Isso não é necessário, mas uma imagem em foco ajuda a fornecer comentários para o usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




