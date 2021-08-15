---
title: Criando o arquivo de arte primário
description: Criando o arquivo de arte primário
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- criando capas, arquivos de arte primários
- Windows Media Player capas, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, imagens primárias
- Windows Media Player capas, imagens primárias
- capas, imagens primárias
- imagens primárias em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21483e9b39692ad9eee7eb2cd7958f2fa70ddb7c2926877b84f3f537156bd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341488"
---
# <a name="creating-the-primary-art-file"></a>Criando o arquivo de arte primário

O arquivo de arte principal conterá a arte que o usuário da sua capa vê pela primeira vez. Nesse caso, você criará imagens em diferentes camadas do programa de arte. O motivo para usar camadas é que você copiará camadas específicas posteriormente para criar arquivos de mapa e arquivos de arte alternativos.

Para criar o arquivo de arte primário, você criará as seguintes camadas na seguinte ordem:

Camada de plano de fundo da capa

Essa é a cor que será transparente quando a capa for exibida. Crie uma camada para isso primeiro, mas escolha a cor final dessa camada depois de escolher uma cor para a camada de contêiner de capa. Essa cor deve ser semelhante, mas não a mesma que a camada de contêiner de capa, para ocultar quaisquer efeitos anti-aliasing.

Camada de contêiner de capa

Essa é a imagem que formará o contorno da sua capa e será o que o usuário vê. Ele também será o contêiner para os dois botões neste exemplo. Pense em sua capa como um contêiner para controles de interface do usuário, como botões, controles deslizantes e assim por diante. Neste exemplo, o contêiner é uma oval amarela.

Camadas do botão Reproduzir e Fechar

Esses são os dois controles de interface do usuário que este exemplo usa. Você os colocará em camadas separadas para que possa ajustá-las facilmente ou copiá-las mais tarde.

Antes de criar suas camadas, você deve criar o arquivo que conterá suas camadas. Inicie o Photoshop e crie um arquivo com 100 pixels de altura e 200 pixels de largura. O arquivo usado para criar a arte para este exemplo é chamado tiny.psd e está incluído no SDK.

Todas as instruções são fornecidas em termos de Limited, mas qualquer outro programa de arte pode ser usado para criar capas, desde que você possa salvar em um dos formatos de arquivo com suporte pelo Windows Media Player (BMP, GIF, JPG e PNG). Você encontrará uma criação de capa mais fácil se usar um programa de arte que tenha camadas, como Adobe Adobe, Jasc Paint Shop Pro ou Jedor Ltdity. As camadas são extremamente úteis porque as imagens devem ser alinhadas corretamente para mapeamento de imagem e exibição de imagens alternativas.

## <a name="skin-background-layer"></a>Camada de plano de fundo da capa

Crie uma nova camada e nomee-a como "Plano de fundo da capa". Isso se tornará a cor de transparência que você definirá no arquivo de definição de capa. Aguarde até que a cor do contêiner de capa seja escolhida antes de preencher a camada da tela de fundo da capa com uma cor específica.

## <a name="skin-container-layer"></a>Camada de contêiner de capa

Em seguida, crie uma nova camada e chame-a de "Contêiner de capa". Isso definirá as bordas da sua capa e será o contêiner para os botões.

Escolha uma cor de primeiro plano para a forma, usando os controles deslizantes de cores da Web. Neste exemplo, a cor " \# DBDD11" foi escolhida.

Em seguida, crie uma forma oval. A maneira mais fácil é usar a ferramenta Eliptical Marquee e criar uma seleção oval. Quando você tiver criado uma seleção oval que seja o tamanho e a forma que você deseja, preencha a seleção com a cor de primeiro plano e cancele a seleção.

Por fim, para tornar isso um pouco mais interessante, aplique o efeito de camada de Bevel e Emboss com os valores padrão.

Sua camada de contêiner de capa deve se parecer com a ilustração a seguir.

![camada de contêiner de capa](images/g01cont.png)

## <a name="background-skin-color"></a>Cor da capa da tela de fundo

Agora que você escolheu uma cor de primeiro plano para sua forma de contêiner de capa, você pode escolher uma cor semelhante para a camada da tela de fundo da capa. Você não quer exatamente a mesma cor ou seu contêiner de capa também será transparente. Na verdade, não use essa cor exata em nenhum outro lugar da sua capa, mesmo em fotografias, porque sempre que essa cor aparecer, a imagem da área de trabalho será exibida.

Você deseja uma cor perto da cor do contêiner de capa para evitar efeitos de suavização. Por exemplo, se você tiver um plano de fundo preto, alguns bits de preto poderão aparecer em torno da borda da sua capa. Ao escolher uma cor próxima à cor do contêiner de capa, todos os pixels perdidos que aparecem no processo de suavização passarão despercebidas.

A suavização é o processo de suavizar as bordas de formas curvadas ou desarmadas. O suavização cria novas cores, para pixels ao longo das bordas de uma forma, que são uma combinação da cor de primeiro plano e da cor da tela de fundo. Algumas dessas cores entre elas podem fazer com que os pixels sejam perdido quando a cor da tela de fundo se tornou transparente.

A camada de fundo da capa deve se parecer com a ilustração a seguir.

![camada de capa da plano de fundo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Camadas de botão Reproduzir e Fechar

Crie uma nova camada e nomee-a como "Botão Fechar". Usando a ferramenta de seleção de Marca elíptica novamente, crie um círculo e posicione-o no lado esquerdo da imagem geral. A ligue a visibilidade do arquivo de contêiner de capa para ajudar a colocar a seleção.

Quando estiver satisfeito com o posicionamento, preencha a seleção com qualquer cor (exceto a cor do contêiner de capa ou da tela de fundo da capa). Neste exemplo, uma cor roxa foi escolhida. Você não precisa se lembrar do número da cor. Em seguida, cancele a seleção e aplique outro efeito padrão de camada de Bevel e Emboss. Se você quiser aplicar efeitos que não são da camada ao botão, faça uma cópia do original para uso posterior no mapeamento.

O botão Fechar deve ser parecido com a ilustração a seguir.

![botão de fechamento](images/g01qbut.png)

Crie uma nova camada e nomee-a como "Botão Reproduzir". Use as mesmas técnicas que você fez para o botão Fechar, mas dê a ele uma cor diferente. Nesse caso, uma cor de botão rosa foi escolhida, mas qualquer cor pode ser usada, desde que não seja da mesma cor que o contêiner de capa (porque ele se mesclaria ao contêiner) ou a cor da tela de fundo da capa (porque ela se tornaria transparente).

O botão Reproduzir deve ser parecido com a ilustração a seguir.

![botão reproduzir](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinar camadas e salvar

Agora você está pronto para criar o arquivo de arte principal. Ocultar todas as camadas e mostrar apenas as seguintes camadas, nesta ordem (de cima para baixo):

Botão Reproduzir

Botão Fechar

Contêiner de capa

Plano de fundo da capa

Salve em um novo arquivo usando o comando Salvar uma Cópia no menu Arquivo. Selecione a opção BMP na parte Salvar como da caixa de diálogo Salvar uma Cópia e digite um nome de arquivo ao qual você se referirá posteriormente no arquivo de definição de capa. O ideal é que você salve isso no mesmo diretório que o arquivo de definição de capa. Por exemplo, você pode chamar essa background.bmp. Escolha as configurações padrão e salve o arquivo.

O arquivo de arte principal deve ter esta aparência:

![arquivo de arte primária](images/g01prime.png)

Você usará esse nome de arquivo como o valor para o atributo **backgroundImage** do **elemento VIEW** no arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando sua primeira capa**](building-your-first-skin.md)
</dt> </dl>

 

 




