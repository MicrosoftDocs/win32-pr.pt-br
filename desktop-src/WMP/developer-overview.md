---
title: Visão geral do desenvolvedor
description: Visão geral do desenvolvedor
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player plug-ins,visualizações
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
- assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20988a8cf1b7923699ec9cee7990b99840b8acdf9371e74da5940ddb8fc8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579408"
---
# <a name="developer-overview"></a>Visão geral do desenvolvedor

Do ponto de vista do desenvolvedor, as visualizações são programas de software que levam dados de áudio fornecidos pelo Windows Media Player e convertem esses dados em gráficos que vão agradá-lo. Os principais assuntos que um desenvolvedor precisa entender para criar uma nova visualização são os seguintes:

## <a name="visualization-packaging"></a>Empacotamento de visualização

As visualizações são controles COM que Windows Media Player usa para transformar as formações de onda de áudio em gráficos animados no Microsoft Windows. Os controles COM são empacotados como bibliotecas Windows DLLs (bibliotecas de vínculo dinâmico) da Microsoft e devem ser registrados no Windows registro. Quando Windows Media Player é executado, as visualizações personalizadas registradas são carregadas e exibidas de acordo com as instruções da capa que Windows Media Player está usando.

## <a name="audio-input"></a>Entrada de áudio

Windows Media Player fornece ao código instantâneos de frequência de áudio e dados de forma de onda em intervalos temporados medidos em frações de segundo. O intervalo de instantâneo é determinado internamente pelo Windows Media Player.

## <a name="graphical-output"></a>Saída gráfica

A saída gráfica da visualização é um contexto de Windows microsoft. Essa é uma superfície de desenho Windows padrão que você pode usar sempre que um instantâneo de áudio é fornecido. Todas as informações básicas Windows tecnologia são tomadas por você. Você só precisa desenhar no contexto do dispositivo com os dados de áudio fornecidos.

## <a name="drawing-tools"></a>Ferramentas de desenho

Você pode desenhar no contexto do dispositivo com funções padrão do Microsoft Windows Graphics Device Interface (GDI), usando canetas e pincéis para criar designs que são modificados pelos dados de áudio fornecidos por Windows Media Player. A GDI fornece um conjunto rico de ferramentas de desenho que podem criar muitos tipos de efeitos visuais.

## <a name="programming-language"></a>Linguagem de programação

Microsoft Visual C++ 6.0 e superior é a única linguagem com suporte para criar visualizações personalizadas.

## <a name="plug-in-wizard"></a>Assistente de plug-in

Windows Media Player fornece um assistente COM que você pode adicionar ao Visual C++ que gerará o código subjacente necessário para sua visualização. Não apenas todos os arquivos de origem são fornecidos, mas uma capa de exemplo é gerada para facilitar o teste da visualização. O código gerado cria uma visualização semelhante a Barras, com duas predefinições. Em seguida, você pode modificar o código para criar sua própria visualização. Um arquivo do Registro também é gerado para registrar sua visualização para que Windows Media Player possa carregá-lo.

O tópico a seguir descreve como o código de visualização processa dados de áudio:

-   [Flow de controle](flow-of-control.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre visualizações personalizadas**](about-custom-visualizations.md)
</dt> </dl>

 

 




