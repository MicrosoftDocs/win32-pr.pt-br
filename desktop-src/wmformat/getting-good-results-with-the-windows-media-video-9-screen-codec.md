---
title: Obter bons resultados com o codec de tela Windows Media Video 9
description: Obter bons resultados com o codec de tela Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows SDK de formato de mídia,Windows vídeo de mídia 9 Codec de tela
- AsF (Advanced Systems Format), Windows Media Video 9 Screen codec
- ASF (formato de sistemas avançados), codec Windows vídeo de mídia 9
- codecs,Windows Media Video 9 Screen
- Windows Codec de tela do Vídeo de Mídia 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657cde745f6bfbabe00fe123b493e2eae2afb20ddf40206f781822770a4386f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110426"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Obter bons resultados com o codec de tela Windows Media Video 9

O codec Windows de tela do Vídeo de Mídia 9 foi projetado para produzir vídeo altamente compactado para captura de tela. Como a maior parte da necessidade de captura de tela envolve imagens bastante simples e estáticas, os altos níveis de compactação obtidos geralmente não significam um grande truque na qualidade da imagem. No entanto, cada captura de tela é diferente e a qualidade da imagem resultante pode variar consideravelmente dependendo das circunstâncias.

A melhor maneira de determinar as configurações de perfil para uma sessão de codec de tela é codificar um arquivo de teste usando um fluxo de taxa de bits variável baseado em qualidade. Defina a qualidade como o valor desejado e codificar uma captura de tela como se estivesse gravando o arquivo final. Quando o arquivo for gravado, reproduza-o usando o objeto de leitor assíncrono, fazendo chamadas regulares para [**IWMReaderAdvanced::GetStatistics.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) Ao monitorar o valor do membro **dwBandwidth** da estrutura [**WM READER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada chamada, você pode determinar a taxa de bits aproximada necessária para atingir a qualidade que deseja. Em seguida, você pode usar essa taxa de bits para codificação de taxa de bits constante.

Se você descobrir que a qualidade que deseja requer uma taxa de bits mais alta do que pode ser usada para seu cenário de entrega, tente as técnicas a seguir para obter mais eficiência do codec.

-   Use uma resolução menor para a captura de tela. Capturar uma resolução de tela maior do que você precisa também pode criar confusão para o visualizador apresentando mais informações do que o necessário.
-   Use menos elementos gráficos na captura de tela. O codec Windows de tela do Vídeo de Mídia 9 é otimizado para codificar Windows primitivos e texto com alta qualidade. Normalmente, ocorrem problemas devido a gráficos bit a bit, que geralmente contêm milhares de cores individuais. Quanto menos bitmaps estiver na tela quando você capturar, melhor serão os resultados. Se você não puder eliminar gráficos da captura de tela, há várias maneiras de minimizar o impacto que um bitmap tem na qualidade da imagem:
    -   Reduza o tamanho do gráfico.
    -   Reduza o número de elementos gráficos individuais que aparecem na tela simultaneamente.
    -   Reduza a quantidade de movimento do gráfico. Por exemplo, se o gráfico estiver em uma janela, mantenha a janela o mais estacionária possível.
    -   Evite mover o ponteiro do mouse sobre o gráfico ou arrastar janelas ou outros elementos sobre o gráfico.
-   Use uma taxa de [*quadros mais lenta.*](wmformat-glossary.md) As capturas de tela geralmente podem ser eficazes com taxas de quadros muito baixas (às vezes, até 4 ou 5 quadros por segundo).
-   Reduza a taxa de bits do áudio que o acompanha.

Além disso, o codec não dá suporte ao reizing do retângulo de vídeo. Em outras palavras, se você tentar usar o codec para codificar uma tela 800 x 600 em um retângulo de vídeo 640 x 480, o vídeo resultante terá artefatos significativos que podem tornar grande parte do texto na tela ilegível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando a captura de tela Fluxos**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configurando Fluxos**](configuring-streams.md)
</dt> </dl>

 

 




