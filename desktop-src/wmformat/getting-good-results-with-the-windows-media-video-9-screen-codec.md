---
title: Obtendo bons resultados com o codec de tela do Windows Media Video 9
description: Obtendo bons resultados com o codec de tela do Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- SDK do Windows Media Format, codec de tela do Windows Media Video 9
- ASF (Advanced Systems Format), codec de tela do Windows Media Video 9
- ASF (formato de sistemas avançados), codec de tela do Windows Media Video 9
- codecs, tela do Windows Media Video 9
- Codec de tela do Windows Media Video 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917008"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Obtendo bons resultados com o codec de tela do Windows Media Video 9

O codec de tela do Windows Media Video 9 foi projetado para produzir vídeo altamente compactado para captura de tela. Como a maior parte da necessidade de captura de tela envolve imagens razoavelmente simples e estáticas, os altos níveis de compactação obtidos geralmente não significam um grande sacrifício na qualidade da imagem. No entanto, cada captura de tela é diferente e a qualidade da imagem resultante pode variar consideravelmente dependendo das circunstâncias.

A melhor maneira de determinar as configurações de perfil para uma sessão de codec de tela é codificar um arquivo de teste usando um fluxo de taxa de bits variável com base em qualidade. Defina a qualidade para o valor desejado e codifique uma captura de tela como se estivesse gravando o arquivo final. Quando o arquivo for gravado, execute-o usando o objeto leitor assíncrono, fazendo chamadas regulares para [**IWMReaderAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). Ao monitorar o valor do membro **dwBandwidth** da estrutura de [**\_ \_ estatísticas do WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada chamada, você pode determinar a taxa de bits aproximada necessária para atingir a qualidade desejada. Em seguida, você pode usar essa taxa de bits para a codificação de taxa de bits constante.

Se você descobrir que a qualidade desejada requer uma taxa de bits maior do que você pode usar para o cenário de entrega, você pode tentar as técnicas a seguir para obter mais eficiência do codec.

-   Use uma resolução menor para a captura de tela. Capturar uma resolução de tela maior do que você precisa também pode criar confusão para o visualizador apresentando mais informações do que o necessário.
-   Use menos elementos gráficos na captura de tela. O codec de tela do Windows Media Video 9 é otimizado para codificar primitivos e texto do Windows com alta qualidade. Geralmente, ocorrem problemas devido a gráficos de bitmap, que geralmente contêm milhares de cores individuais. Quanto menos bitmaps estiverem na tela quando você capturar, melhor será seus resultados. Se você não puder eliminar gráficos da captura de tela, há várias maneiras de minimizar o impacto que um bitmap tem na qualidade da imagem:
    -   Reduza o tamanho do gráfico.
    -   Reduza o número de gráficos individuais que aparecem na tela simultaneamente.
    -   Reduza a quantidade de movimento do gráfico. Por exemplo, se o elemento gráfico estiver em uma janela, mantenha a janela como estático como possível.
    -   Evite mover o ponteiro do mouse sobre o gráfico ou arrastar o Windows ou outros elementos sobre o gráfico.
-   Use uma taxa de [*quadros*](wmformat-glossary.md)mais lenta. Capturas de tela geralmente podem ser eficazes em taxas de quadros muito baixas (às vezes, com 4 ou 5 quadros por segundo).
-   Reduza a taxa de bits do áudio que o acompanha.

Além disso, o codec não oferece suporte ao redimensionamento do retângulo de vídeo. Em outras palavras, se você tentar usar o codec para codificar uma tela de 800 x 600 para um retângulo de vídeo 640 x 480, o vídeo resultante terá artefatos significativos que podem tornar grande parte do texto na tela ilegível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos de captura de tela**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




