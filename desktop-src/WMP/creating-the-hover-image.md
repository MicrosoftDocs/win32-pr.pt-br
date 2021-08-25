---
title: Criando a imagem em foco
description: Criando a imagem em foco
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- Criando capas, imagens em foco
- Windows Media Player capas, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, imagens em foco
- Windows Media Player capas, imagens em foco
- capas, imagens em foco
- imagens em foco em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88eff91123a28dae94425d7ea6e7591462545a2d7da0372b088eeec6bd67ed60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902276"
---
# <a name="creating-the-hover-image"></a>Criando a imagem em foco

A imagem principal dessa capa é de dois botões em uma elipse. Para dar ao usuário uma pista sobre o que fazer, você pode adicionar imagens em foco. Essas são imagens alternativas que são exibidas quando o usuário passa o mouse sobre um botão. Os botões de foco também conterão os símbolos de controle de videocassete Play e Stop para que os usuários saibam exatamente o que eles podem fazer. O uso de imagens em foco permite criar capas informativas complexas e de autodocumentação.

Para criar a imagem em foco, você precisará usar os dois botões criados para o arquivo de arte principal, copiá-los para novas camadas e adicionar mais camadas ao texto. Use as seguintes etapas:

1.  Copie a camada de botão fechar e renomeie-a "fechar mouse".
2.  Use o seletor de cores para criar uma cor de primeiro plano de um amarelo claro ( \# CCFF33). Isso foi escolhido para contraste com as cores do botão. em seguida, use a ferramenta Lata de Tinta para preencher o interior do círculo na camada fechar foco.
3.  Copie a camada do botão Play e renomeie-a "Play hover".
4.  Use a ferramenta Lata de Tinta para preencher o interior do círculo na camada reproduzir foco com a mesma cor do círculo de fechamento de foco.
5.  Crie uma nova camada e nomeie-a como "fechar quadrado". Use o seletor de cores para criar uma cor de primeiro plano de azul escuro. Use a ferramenta caneta para desenhar um quadrado, transformá-lo em uma seleção, preenchê-lo e excluir o caminho. Usando a ferramenta mover, mova o quadrado e centralize-o sobre o botão de fechamento em foco.
6.  Crie uma nova camada e nomeie-a como "reproduzir triângulo". Use a ferramenta caneta para criar o triângulo para "reproduzir" usando as mesmas técnicas que você fez para criar a camada quadrada de fechamento. Centralize-o no botão Play hover.

Agora você está pronto para criar o arquivo de arte de foco. Oculte todas as camadas e, em seguida, mostre apenas as camadas a seguir, nesta ordem (de cima para baixo):

Reproduzir triângulo

Fechar quadrado

Passar o mouse

Fechar foco

Salve em um novo arquivo usando o comando salvar uma cópia no menu arquivo. Selecione a opção BMP na parte salvar como da caixa de diálogo salvar uma cópia e digite um nome de arquivo que você irá referenciar posteriormente no arquivo de definição de capa. O ideal é que você salve isso no mesmo diretório que o arquivo de definição de capa. Por exemplo, você pode chamar essa hover.bmp. Escolha as configurações padrão e salve o arquivo.

O arquivo de arte de foco deve ser semelhante à ilustração a seguir.

![imagem em foco](images/absam01h.png)

O botão de foco amarelo será exibido no lugar do botão normal. Se você passar o mouse sobre o botão direito em sua capa, o botão amarelo rotulado como "reproduzir" aparecerá e, se você passar o mouse sobre o botão esquerdo, o usuário verá "fechar". As duas imagens em foco nunca serão exibidas ao mesmo tempo, porque o mouse não pode focalizar os dois botões ao mesmo tempo. Você deve ligar o mouse e ter um arquivo artístico focalizado que corresponda às áreas dos arquivos de mapeamento em áreas do arquivo em foco.

Quando você salvar o arquivo, o nome de arquivo escolhido será usado posteriormente como o valor do atributo **hoverImage** do elemento de grupo de **botões** em seu arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando sua primeira capa**](building-your-first-skin.md)
</dt> </dl>

 

 




