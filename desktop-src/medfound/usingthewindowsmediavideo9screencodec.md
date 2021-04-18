---
description: Usando o codec de tela do Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Usando o codec de tela do Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759685"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Usando o codec de tela do Windows Media Video 9 (Microsoft Media Foundation)

O codec de tela do Windows Media Video 9 é otimizado para compactação de *vídeo do aplicativo*, que consiste em capturas de tela consecutivas para uma exibição do computador. O codec aproveita a simplicidade da imagem típica (relativamente poucas cores, muitas linhas retas e assim por diante) e a falta de movimento relativa para atingir uma taxa de compactação muito alta. A desvantagem dessa otimização é que o vídeo que não está em conformidade com as características esperadas do vídeo do aplicativo pode ser difícil de compactar com um nível aceitável de qualidade.

O codificador de tela do Windows Media Video 9 é identificado pelo CLSID do identificador de classe \_ CMSSEncMediaObject2, e o decodificador é identificado como o CLSID do identificador de classe \_ CMSSDecMediaObject. O valor FOURCC para os tipos de mídia usando esse codec é "MSS2".

## <a name="configuring-the-encoder"></a>Configurando o codificador

O codificador do codec de tela do Windows Media Video 9 é configurado da mesma forma que o decodificador de vídeo padrão.

> [!Note]  
> O codificador de tela dá suporte apenas à codificação de uma passagem. Você pode definir a propriedade [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) como 2 e processar as entradas duas vezes sem erro, mas não há nenhum benefício para fazer isso. Esse é um problema conhecido e pode ser corrigido em versões futuras.

 

## <a name="getting-the-best-results"></a>Obtendo os melhores resultados

Se você descobrir que a qualidade desejada em seu conteúdo de captura de tela requer uma taxa de bits maior do que você pode usar para o cenário de entrega, você pode tentar as seguintes técnicas para obter mais eficiência do Codec:

-   Use uma resolução menor para a captura de tela. Capturar uma resolução de tela maior do que o necessário pode confundir o visualizador apresentando informações desnecessárias.
-   Use uma taxa de quadros mais lenta. Capturas de tela geralmente podem ser eficazes em taxas de quadros muito baixas (às vezes, com 4 ou 5 quadros por segundo).
-   Use menos elementos gráficos na captura de tela. O codec de tela do Windows Media Video 9 é otimizado para codificar primitivos e texto do Windows com alta qualidade. Geralmente, ocorrem problemas devido a gráficos de bitmap, que geralmente contêm milhares de cores individuais. Quanto menos bitmaps estiverem na tela quando você capturar, melhor será seus resultados. Se você não puder eliminar gráficos da captura de tela, há várias maneiras de minimizar o impacto que um bitmap tem na qualidade da imagem:
    -   Reduza o tamanho do gráfico.
    -   Reduza o número de gráficos individuais que aparecem na tela ao mesmo tempo.
    -   Reduza a quantidade de movimento do gráfico. Por exemplo, se o elemento gráfico estiver em uma janela, mantenha a janela como estático como possível.
    -   Evite mover o ponteiro do mouse sobre o gráfico ou arrastar o Windows ou outros elementos sobre o gráfico.

## <a name="decoding"></a>Decodificação

Não há requisitos especiais para decodificar vídeo de captura de tela. No entanto, assim como acontece com todos os codecs do Windows Media Video 9, o decodificador de captura de tela não pode descompactar corretamente o conteúdo codificado sem os dados privados do codec.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a codificação de vídeo](configuringvideoencoding.md)
</dt> <dt>

[Usando dados privados do codec de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Codificador de tela do Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



