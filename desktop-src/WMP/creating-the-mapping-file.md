---
title: Criando o arquivo de mapeamento
description: Criando o arquivo de mapeamento
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- Criando capas, mapeando arquivos
- Capas do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, mapeando imagens
- Capas do Windows Media Player, mapeando imagens
- capas, mapeando imagens
- Mapeando imagens em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363678"
---
# <a name="creating-the-mapping-file"></a>Criando o arquivo de mapeamento

Depois de criar as partes do seu arquivo de arte principal, é relativamente fácil criar um arquivo de mapeamento. Você criará o novo arquivo de mapeamento combinando a arte das duas camadas de botão que você já criou.

1.  Você precisará usar os dois botões criados para o arquivo de arte primário e copiá-los para uma nova camada. Use as seguintes etapas: copiar a camada do botão fechar, remover quaisquer efeitos de camada e renomeá-lo como "fechar mapa". A arte deve parecer simples, sem bisels.
2.  Use o seletor de cores para criar uma cor de primeiro plano de vermelho puro. Verifique se o valor do número de cor é " \# FF0000". Em seguida, use a ferramenta Lata de Tinta para preencher o interior do círculo da camada fechar mapa.
3.  Copie a camada do botão reproduzir, remova todos os efeitos da camada e renomeie-o como "mapa de reprodução". Novamente, a arte deve parecer simples. Você não deseja nenhum efeito na camada de mapeamento porque está apenas definindo regiões do bitmap que o Windows Media Player usará para determinar onde o mouse executa uma ação e o que você deseja fazer com ela.
4.  Use o seletor de cores para criar uma cor de primeiro plano de verde puro. Verifique se o valor do número de cor é " \# 00FF00". Em seguida, use a ferramenta Lata de Tinta para preencher o interior do círculo da camada do mapa de reprodução.

Agora você está pronto para criar o arquivo de arte de mapeamento. Oculte todas as camadas e, em seguida, mostre apenas as camadas a seguir, nesta ordem (de cima para baixo):

Reproduzir mapa

Fechar mapa

Salve em um novo arquivo usando o comando salvar uma cópia no menu arquivo. Selecione a opção BMP na parte salvar como da caixa de diálogo salvar uma cópia e digite um nome de arquivo que você irá referenciar posteriormente no arquivo de definição de capa. O ideal é que ele esteja no mesmo diretório que o arquivo de definição de capa. Por exemplo, você pode chamar esse arquivo map.bmp. Escolha as configurações padrão e salve o arquivo.

O arquivo de mapeamento deve ser semelhante à ilustração a seguir.

![mapping file](images/g01map.png)

Como você pode imaginar, a área verde será usada para determinar quando fazer o Windows Media Player iniciar e a área vermelha para informá-lo para parar. Todas as duas cores podem ser usadas, desde que você use os números de cor ao configurar o arquivo de definição de capa. Verifique se as cores no mapa são cores puras para a região que você deseja usar e têm bordas distintas. Uma cor pura seria aquela em que cada pixel na área tem o mesmo valor de cor. O uso de um efeito pode desfocar ou distorcer a borda, modificando ligeiramente as cores de alguns dos pixels. O arquivo de mapeamento só é visto pelo mouse, não por um homem, portanto não se preocupe com a decoração e remova quaisquer efeitos de camada que você possa ter feito de outras camadas.

Quando você salvar o arquivo, o nome de arquivo escolhido será usado posteriormente como o valor do atributo **mappingImage** do elemento de grupo de **botões** em seu arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando sua primeira capa**](building-your-first-skin.md)
</dt> </dl>

 

 




