---
description: Quando você fornece uma miniatura, as diretrizes a seguir devem ser seguidas.
title: Diretrizes do manipulador de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: 9763c9cb859df3530766b6e65f9dce4f7de87fd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/11/2020
ms.locfileid: "104085014"
---
# <a name="thumbnail-handler-guidelines"></a>Diretrizes do manipulador de miniaturas

Quando você fornece uma miniatura, as diretrizes a seguir devem ser seguidas.

-   Forneça miniaturas que são bem exibidas em uma resolução de pixels 256x256s na cor de 32 bits. Uma miniatura desse tamanho é usada pelo painel de leitura do Windows Vista na ausência de um Gerenciador de visualização registrado. No entanto, um Gerenciador de visualização é a opção preferida e deve ser fornecido sempre que possível.
-   Quando você cria várias imagens de tamanhos diferentes, não crie imagens menores a partir do maior cortando a página, o quadro ou a imagem. Reduza verticalmente a imagem inteira.
-   Não mostrar várias páginas, quadros ou imagens de uma só vez; Basta usar um. Se um documento consistir em várias páginas, como um documento de texto ou uma planilha que consiste em várias planilhas, a página de rosto geralmente é a melhor opção, mas independentemente da qual você usa, use apenas uma. Não agregue páginas diferentes, o que dá uma aparência desorganizada.
-   O Windows Vista é responsável por dimensionar ou reduzir as imagens de amostragem. Se o seu manipulador for solicitado por uma imagem maior do que a disponível, forneça o tamanho mais próximo que você tem. Não tente redimensionar dinamicamente sua própria imagem.
-   Sempre retorne uma imagem em miniatura do manipulador em vez de executar uma lógica especial para retornar ícones tradicionais. Abaixo de um determinado tamanho, o Windows Vista exibe automaticamente um ícone tradicional no lugar da miniatura. Consulte a seção *cache em miniatura e dimensionamento* de [manipuladores de miniatura](thumbnail-providers.md) para obter mais detalhes.
-   Sempre retorna uma miniatura com a taxa de proporção da página, do quadro ou da imagem. Não use alfa para concluir um quadrado. O Windows Vista é responsável por posicionar corretamente uma imagem não quadrada.
-   Não adicione adornos às suas miniaturas. O Windows Vista aplica automaticamente as sombras de soltar e outros adornos quando apropriado. Ele também aplica adornos especiais para tipos de arquivo específicos, como imagens ou vídeos.
-   Não sobreponha as informações do tipo de arquivo ou do aplicativo em sua miniatura. O Windows Vista exibe uma sobreposição de tipo para você no canto inferior direito da imagem. Essa sobreposição se baseia no tipo percebido, mas pode ser definida para tipos de arquivo individuais.
-   Para obter melhor desempenho, quando a miniatura se baseia no conteúdo do arquivo — uma página de um documento, por exemplo, armazena a imagem de visualização quando o arquivo é salvo (e, portanto, provavelmente alterado) em vez de calcular isso em tempo real. Isso deve ser feito se o cálculo for de uso intensivo de memória (mais de um ou dois segundos). Se isso não for feito, as exibições que mostram um grande número de arquivos cujas miniaturas são manipuladas por diferentes manipuladores levarão algum tempo para serem exibidas — uma experiência de usuário inválida. O Windows Vista armazena em cache miniaturas e refere-se à hora da última modificação para determinar se uma miniatura deve ser atualizada.
-   Lembre-se de que o Explorer pode optar por não exibir uma miniatura mesmo se um provedor estiver disponível. Por exemplo, um arquivo que foi arquivado em fita não será rechamado para obter sua miniatura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipuladores de miniatura](thumbnail-providers.md)
</dt> <dt>

[Criando manipuladores de miniatura](building-thumbnail-providers.md)
</dt> </dl>

 

 



