---
title: Visão geral do desenvolvedor
description: Visão geral do desenvolvedor
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-ins do Windows Media Player, visualizações
- plug-ins, visualizações
- visualizações, visão geral do desenvolvedor
- visualizações personalizadas, visão geral do desenvolvedor
- visualizações, controles COM
- visualizações personalizadas, controles COM
- visualizações, entrada de áudio
- visualizações personalizadas, entrada de áudio
- visualizações, saída gráfica
- visualizações personalizadas, saída gráfica
- visualizações, ferramentas de desenho
- visualizações personalizadas, ferramentas de desenho
- visualizações, linguagem de programação
- visualizações personalizadas, linguagem de programação
- visualizações, Visual C++
- visualizações personalizadas, Visual C++
- visualizações, assistente de plug-in
- visualizações personalizadas, assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292468"
---
# <a name="developer-overview"></a>Visão geral do desenvolvedor

Do ponto de vista do desenvolvedor, as visualizações são programas de software que pegam os dados de áudio fornecidos pelo Windows Media Player e convertem esses dados em elementos gráficos que serão o olho do usuário. Os principais assuntos que um desenvolvedor precisa entender para criar uma nova visualização são os seguintes:

## <a name="visualization-packaging"></a>Empacotamento de visualização

As visualizações são controles COM que o Windows Media Player usa para ativar as ondas de forma de áudio em gráficos animados no Microsoft Windows. Os controles COM são empacotados como DLLs (bibliotecas de vínculo dinâmico) do Microsoft Windows e devem ser registrados no registro do Windows. Quando o Windows Media Player é executado, as visualizações personalizadas registradas são carregadas e exibidas de acordo com as instruções da capa que o Windows Media Player está usando.

## <a name="audio-input"></a>Entrada de áudio

O Windows Media Player fornece seu código com instantâneos de frequência de áudio e dados de formato de onda em intervalos de tempo medidos em frações de um segundo. O intervalo de instantâneos é determinado internamente pelo Windows Media Player.

## <a name="graphical-output"></a>Saída gráfica

A saída gráfica de sua visualização é um contexto de dispositivo do Microsoft Windows. Essa é uma superfície de desenho padrão do Windows que você pode desenhar sempre que um instantâneo de áudio é fornecido. Toda a tecnologia Windows em segundo plano é levada em sua atenção. Basta desenhar no contexto do dispositivo com os dados de áudio fornecidos.

## <a name="drawing-tools"></a>Ferramentas de desenho

Você pode desenhar no contexto do dispositivo com funções padrão do Microsoft Windows Graphics Device Interface (GDI), usando canetas e pincéis para criar designs que são modificados pelos dados de áudio fornecidos para você pelo Windows Media Player. O GDI fornece um rico conjunto de ferramentas de desenho que podem criar muitos tipos de efeitos visuais.

## <a name="programming-language"></a>Linguagem de programação

Microsoft Visual C++ 6,0 e superior é a única linguagem com suporte para a criação de visualizações personalizadas.

## <a name="plug-in-wizard"></a>Assistente de plug-in

O Windows Media Player fornece um assistente COM que você pode adicionar ao Visual C++ que irá gerar o código subjacente necessário para sua visualização. Não apenas todos os arquivos de origem são fornecidos, mas uma amostra de aparência é gerada para facilitar o teste da visualização. O código gerado cria uma visualização semelhante a barras, com duas predefinições. Em seguida, você pode modificar o código para criar sua própria visualização. Um arquivo de registro também é gerado para registrar sua visualização para que o Windows Media Player possa carregá-lo.

O tópico a seguir descreve como o código de visualização processa os dados de áudio:

-   [Fluxo de controle](flow-of-control.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre visualizações personalizadas**](about-custom-visualizations.md)
</dt> </dl>

 

 




