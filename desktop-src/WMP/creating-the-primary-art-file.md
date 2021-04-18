---
title: Criando o arquivo de arte principal
description: Criando o arquivo de arte principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Criando capas, arquivos de arte principais
- Capas do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, imagens primárias
- Capas do Windows Media Player, imagens primárias
- capas, imagens primárias
- imagens primárias em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570562"
---
# <a name="creating-the-primary-art-file"></a>Criando o arquivo de arte principal

O arquivo de arte principal conterá a arte que o usuário da sua capa vê primeiro. Nesse caso, você criará imagens em camadas diferentes do seu programa de arte. O motivo para usar camadas é que você copiará camadas específicas posteriormente para criar arquivos de mapa e arquivos de arte alternativos.

Para criar o arquivo de arte principal, você criará as seguintes camadas na seguinte ordem:

Camada de fundo de capa

Essa é a cor que será transparente quando a capa for exibida. Crie uma camada para isso primeiro, mas escolha a cor final dessa camada depois de escolher uma cor para a camada de contêiner de capa. Essa cor deve ser semelhante a, mas não a mesma que a camada de contêiner de capa, para ocultar quaisquer efeitos de suavização de alias.

Camada de contêiner de capa

Essa é a imagem que formará o contorno da sua capa e será o que o usuário vê. Ele também será o contêiner para os dois botões neste exemplo. Imagine sua capa como um contêiner para controles de interface do usuário, como botões, controles deslizantes e assim por diante. Neste exemplo, o contêiner é uma elipse amarela.

Reproduzir e fechar camadas de botão

Esses são os dois controles de interface do usuário que este exemplo usa. Você os colocará em camadas separadas para que possa ajustá-las facilmente ou copiá-las mais tarde.

Antes de criar suas camadas, você deve criar o arquivo que manterá suas camadas. Inicie o Photoshop e crie um novo arquivo com 100 pixels de altura e 200 pixels de largura. O arquivo usado para criar a arte para este exemplo é chamado de tiny.psd e está incluído no SDK.

Todas as instruções são fornecidas em termos do Photoshop, mas qualquer outro programa de arte pode ser usado para criar capas, desde que você possa salvar em um dos formatos de arquivo com suporte no Windows Media Player (BMP, GIF, JPG e PNG). Você encontrará uma criação de capa mais fácil se usar um programa de arte que tenha camadas, como Adobe Photoshop, Jasc Paint Shop Pro ou Jedor viscosity. As camadas são extremamente úteis porque as imagens devem estar alinhadas corretamente para o mapeamento de imagem e a exibição de imagens alternativas.

## <a name="skin-background-layer"></a>Camada de fundo de capa

Crie uma nova camada e nomeie-a como "fundo da capa". Isso se tornará a cor de transparência que você definirá no arquivo de definição de capa. Aguarde até que a cor do contêiner de capa seja escolhida antes de preencher a camada de plano de fundo da capa com uma cor específica.

## <a name="skin-container-layer"></a>Camada de contêiner de capa

Em seguida, crie uma nova camada e chame-a de "contêiner de capa". Isso definirá as bordas da sua capa e será o contêiner para os botões.

Escolha uma cor de primeiro plano para a forma, usando os controles deslizantes de cores da Web. Neste exemplo, a cor " \# DBDD11" foi escolhida.

Em seguida, crie uma forma oval. A maneira mais fácil é usar a ferramenta Eliptical Marquee e criar uma seleção de oval. Quando você tiver criado uma seleção de oval que é o tamanho e a forma desejados, preencha a seleção com a cor de primeiro plano e cancele a seleção.

Por fim, para tornar essa aparência um pouco mais interessante, aplique o efeito de camada de bisel e entalhe com os valores padrão.

Sua camada de contêiner de capa deve ser parecida com a ilustração a seguir.

![camada de contêiner de capa](images/g01cont.png)

## <a name="background-skin-color"></a>Cor da capa em segundo plano

Agora que você escolheu uma cor de primeiro plano para sua forma de contêiner de capa, você pode escolher uma cor semelhante para sua camada de plano de fundo de capa. Você não quer exatamente a mesma cor ou seu contêiner de capa também será transparente. Na verdade, certifique-se de não usar essa cor exata em qualquer outro lugar na sua capa, mesmo em fotografias, porque sempre que essa cor é exibida, a imagem da área de trabalho será exibida em vez disso.

Você deseja uma cor próxima à cor do contêiner da capa para evitar efeitos de suavização de alias. Por exemplo, se você tiver um plano de fundo preto, alguns bits de preto poderão aparecer em toda a borda da sua capa. Ao escolher uma cor perto da cor do contêiner de capa, todos os pixels isolados que aparecem no processo de suavização de serrilhado serão despercebidos.

A suavização de serrilhado é o processo de suavização das bordas de formas inclinadas ou curvas. A suavização de serrilhado cria novas cores, para pixels ao longo das bordas de uma forma, que são uma mistura da cor do primeiro plano e da cor do plano de fundo. Algumas dessas cores podem fazer com que os pixels sejam perdidos quando a cor do plano de fundo se torna transparente.

Sua camada de plano de fundo de capa deve ser parecida com a ilustração a seguir.

![camada de capa em segundo plano](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Reproduzir e fechar camadas de botão

Crie uma nova camada e nomeie-a como "Fechar botão". Usando a ferramenta de seleção de letreiro Eliptical novamente, crie um círculo e posicione-o no lado esquerdo da imagem geral. Ative a visibilidade do arquivo de contêiner de capa para ajudar a colocar a seleção.

Quando estiver satisfeito com o posicionamento, preencha a seleção com qualquer cor (exceto a cor do contêiner da capa ou do plano de fundo da capa). Neste exemplo, foi escolhida uma cor roxa. Você não precisa se lembrar do número da cor. Em seguida, cancele a seleção e aplique outro efeito de camada de chanfro e entalhe padrão. Se você quiser aplicar efeitos de não camada ao botão, faça uma cópia do original para uso posterior no mapeamento.

O botão fechar deve ser semelhante à ilustração a seguir.

![botão de fechamento](images/g01qbut.png)

Crie uma nova camada e nomeie-a como "botão reproduzir". Use as mesmas técnicas que você fez para o botão fechar, mas dê a ela uma cor diferente. Nesse caso, uma cor de botão rosa foi escolhida, mas qualquer cor pode ser usada desde que ela não seja a mesma cor que o contêiner de capa (porque ela se misturaria no contêiner) ou a cor de fundo da capa (porque ela se tornaria transparente).

O botão de reprodução deve ser semelhante à ilustração a seguir.

![botão reproduzir](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Combinar camadas e salvar

Agora você está pronto para criar o arquivo de arte primário. Oculte todas as camadas e, em seguida, mostre apenas as camadas a seguir, nesta ordem (de cima para baixo):

Botão reproduzir

Botão Fechar

Contêiner de capa

Plano de fundo da capa

Salve em um novo arquivo usando o comando salvar uma cópia no menu arquivo. Selecione a opção BMP na parte salvar como da caixa de diálogo salvar uma cópia e digite um nome de arquivo que você irá referenciar posteriormente no arquivo de definição de capa. O ideal é que você salve isso no mesmo diretório que o arquivo de definição de capa. Por exemplo, você pode chamar essa background.bmp. Escolha as configurações padrão e salve o arquivo.

O arquivo de arte principal deve ter a seguinte aparência:

![arquivo de arte principal](images/g01prime.png)

Você usará esse nome de arquivo como o valor para o atributo **backgroundImage** do elemento **View** em seu arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando sua primeira capa**](building-your-first-skin.md)
</dt> </dl>

 

 




