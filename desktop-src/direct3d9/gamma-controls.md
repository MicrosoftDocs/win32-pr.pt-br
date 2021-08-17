---
description: Os controles gama permitem alterar o modo como o sistema exibe o conteúdo da superfície, sem afetar o conteúdo da superfície em si.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Controles gama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074f60199364ba86a0b5ad743fcc03121351cad0ac071d9231beef7c7156f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122195"
---
# <a name="gamma-controls-direct3d-9"></a>Controles gama (Direct3D 9)

Os controles gama permitem alterar o modo como o sistema exibe o conteúdo da superfície, sem afetar o conteúdo da superfície em si. Imagine esses controles como filtros muito simples que o Direct3D aplica aos dados à medida que deixa uma superfície e antes de ser renderizado na tela.

Os controles gama são uma propriedade de uma cadeia de permuta. Os controles gama possibilitam alterar dinamicamente como os níveis vermelho, verde e azul da superfície são mapeados para os níveis reais que o sistema exibe. Ao definir os níveis de gama, você pode fazer com que a tela do usuário pisque cores-vermelho quando o caractere do usuário é capturado, verde quando o caractere pega um novo item e assim por diante, sem copiar novas imagens para o buffer de quadro para obter o efeito. Ou, você pode ajustar os níveis de cor para aplicar uma tendência de cor às imagens no buffer de fundo.

Sempre há pelo menos uma cadeia de permuta (a cadeia de permuta implícita) para cada dispositivo porque o Direct3D 9 tem uma cadeia de permuta como uma propriedade do dispositivo. Como a rampa de gama é uma propriedade da cadeia de permuta, a rampa de gama pode ser aplicada quando a cadeia de permuta é janelada. A rampa de gama entra em vigor imediatamente. Não há nenhuma espera por uma operação de sincronização vertical.

Os métodos [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) e [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) permitem manipular níveis de Rampes que afetam os componentes de cores vermelho, verde e azul dos pixels da superfície antes de serem enviados ao conversor digital para analógico (DAC) para exibição.

## <a name="gamma-ramp-levels"></a>Níveis de rampa gama

No Direct3D, o termo faixa gama descreve um conjunto de valores que mapeiam o nível de um componente de cor específico-vermelho, verde, azul-para todos os pixels no buffer de quadro para novos níveis que são recebidos pelo DAC para exibição. O remapeamento é executado por meio de três tabelas de pesquisa, uma para cada componente de cor.

Veja como funciona: o Direct3D usa um pixel do buffer de quadro e avalia seus componentes de cor de vermelho, verde e azul individuais. Cada componente é representado por um valor de 0 a 65535. O Direct3D usa o valor original e o usa para indexar uma matriz de elemento 256 (a rampa), em que cada elemento contém um valor que substitui o original. O Direct3D executa esse processo de pesquisa e substituição para cada componente de cor de cada pixel no buffer de quadros, alterando assim as cores finais de todos os pixels na tela.

É útil visualizar os valores de rampa ao grafá-los, conforme mostrado nos dois grafos a seguir. O gráfico esquerdo mostra uma rampa que não modifica as cores. O gráfico à direita mostra uma rampa que impõe uma tendência negativa para o componente de cor ao qual ela é aplicada.

![grafos dos valores de rampa gama](images/gammalv.png)

Os elementos de matriz para o grafo à esquerda contêm valores idênticos ao seu índice-0 no elemento no índice 0 e 65535 no índice 255. Esse tipo de rampa é o padrão, pois ele não altera os valores de entrada antes que eles sejam exibidos. O grafo certo fornece mais variação; sua rampa contém valores que variam de 0 no primeiro elemento a 32768 no último elemento, com valores que variam uniformemente entre eles. O efeito é que o componente de cor que usa essa rampa parece sem áudio na tela. Você não está limitado a usar grafos lineares; Se o seu aplicativo puder atribuir mapeamento arbitrário, se necessário. Você pode até mesmo definir as entradas para todos os zeros para remover completamente um componente de cor da exibição.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Configurando e recuperando os níveis de rampa gama

Os níveis de rampa de gama são efetivamente tabelas de pesquisa que o Direct3D usa para mapear os componentes de cor do buffer de quadros para novos níveis que serão exibidos. Você pode definir e recuperar os níveis de rampa para a superfície primária chamando os métodos [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) e [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) . **SetGammaRamp** aceita dois parâmetros e **GetGammaRamp** aceita um parâmetro. Para **SetGammaRamp**, o primeiro parâmetro é D3DSGR \_ CALIBRATE ou D3DSGR \_ sem \_ calibragem. O segundo parâmetro, pRamp, é um ponteiro para uma estrutura [**D3DGAMMARAMP**](d3dgammaramp.md) . A estrutura **D3DGAMMARAMP** contém matrizes de 3 256 elementos de palavras, uma matriz cada para conter as rampas de gama vermelha, verde e azul. **GetGammaRamp** tem um parâmetro que usa um ponteiro para um tipo **D3DGAMMARAMP** que será preenchido com a rampa de gama atual.

Você pode incluir o \_ valor de calibragem D3DSGR para o primeiro parâmetro de [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) para invocar o calibrador ao definir novos níveis de gama. A calibragem de escalas gama gera uma sobrecarga de processamento e não deve ser usada com frequência. A definição de uma rampa de gama calibrada fornece um valor gama consistente e absoluto para o usuário, independentemente do adaptador de vídeo e do monitor.

Nem todos os sistemas dão suporte à calibragem gama. Para determinar se a calibragem gama tem suporte, chame [**GetDeviceCaps**](/windows/desktop/api)e examine o membro Caps2 da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associada depois que o método retornar. Se o \_ sinalizador de funcionalidade D3DCAPS2 CANCALIBRATEGAMMA estiver presente, a calibração gama terá suporte.

Ao definir novos níveis de ramp, lembre-se de que os níveis definidos nas matrizes são usados apenas quando seu aplicativo está no modo de tela inteira e exclusivo. Sempre que o aplicativo muda para o modo normal, os níveis de rampa são separados, dando efeito novamente quando o aplicativo reabilita o modo de tela inteira.

Se o dispositivo não oferecer suporte a rampas de gama no modo de apresentação atual da cadeia de troca (tela inteira ou em janela), nenhum valor de erro será retornado. Os aplicativos podem verificar os \_ bits de recurso D3DCAPS2 FULLSCREENGAMMA e D3DCAPS2 \_ CANCALIBRATEGAMMA no membro Caps2 do tipo D3DCAPS9 para determinar os recursos do dispositivo e se um calibrador está instalado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
