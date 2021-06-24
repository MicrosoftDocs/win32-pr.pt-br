---
title: Estruturas DirectWrite
description: DirectWrite define as estruturas a seguir.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f678be8e02c8afecd849673d97ae20f6b1a710
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587915"
---
# <a name="directwrite-structures"></a>Estruturas DirectWrite

DirectWrite define as estruturas a seguir.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Representa dados de bitmap no formato BGRA32. |
| [**DWRITE \_ CARET \_ METRICS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | A [**estrutura DWRITE \_ CARET \_ METRICS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) especifica as métricas para o posicionamento de caret em uma fonte. |
| [**DWRITE \_ CLUSTER \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contém informações sobre um cluster de glifo. |
| [**DWRITE \_ COLOR \_ F**](dwrite-color-f.md) | Descreve os componentes vermelho, verde, azul e alfa de uma cor. |
| [**DWRITE \_ COLOR \_ GLIPH \_ RUN**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contém as informações necessárias para renderizar para desenhar as executações de glifo com informações de cor de glifo. |
| [**DWRITE \_ COLOR \_ GLIFO \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Representa uma run de glifo de cor. O método IDWriteFactory4::TranslateColorGlyphRun retorna uma coleção ordenada de glifos de cores de tipos variados, dependendo do que a fonte dá suporte. |
| [**FRAGMENTO DE ARQUIVO \_ DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Representa um intervalo de bytes em um arquivo de fonte. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Representa o intervalo mínimo e máximo dos valores possíveis para um eixo de fonte. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Representa um valor para um eixo de fonte. Usado ao consultar e criar instâncias de fonte. |
| [**RECURSO DE \_ FONTE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Especifica as propriedades usadas para identificar e executar recursos tipográficos no rosto da fonte atual. |
| [**MÉTRICAS DE FONTE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | A [**estrutura DWRITE \_ FONT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) especifica as métricas aplicáveis a todos os glifos na face da fonte. |
| [**DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | A [**estrutura DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) especifica as métricas aplicáveis a todos os glifos na face da fonte. |
| [**PROPRIEDADE DE \_ FONTE DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Propriedade font usada para filtrar conjuntos de fontes e criar um conjunto de fontes com propriedades explícitas. |
| [**DWRITE \_ DADOS DE IMAGEM DE \_ \_ GLIFO**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Dados para um único glifo de GetGlyphImageData. |
| [**DWRITE \_ MÉTRICAS DE \_ GLIFO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Especifica as métricas de um glifo individual. |
| [**DESLOCAMENTO DE \_ GLIFO \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | O ajuste opcional para a posição de um glifo. |
| [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contém as informações necessárias para renderizar para desenhar as executações de glifo. |
| [**DWRITE \_ LYPH \_ RUN \_ DESCRIPTION**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contém propriedades adicionais relacionadas a aquelas [**em DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_MÉTRICAS DE TESTE DE ACERTO \_ \_ DO DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Descreve a região obtida por um teste de acerto. |
| [**DWRITE \_ \_ MÉTRICAS DE OBJETO EM \_ LINHA**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contém propriedades que descrevem a medida geométrica de um objeto em linha definido pelo aplicativo. |
| [**OPORTUNIDADE DE JUSTIFICATIVA \_ DE DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | A [**estrutura DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) especifica informações de justificativa por glifo. |
| [**PONTO DE \_ INTERRUPÇÃO DE LINHA DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Características do ponto de interrupção de linha de um caractere. |
| [**MÉTRICAS DE LINHA DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contém informações sobre uma linha de texto formatada. |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contém informações sobre uma linha de texto formatada. |
| [**ESPAÇAMENTO \_ DE LINHA \_ DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | A [**estrutura DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) especifica a transformação gráfica a ser aplicada aos glifos renderizados. |
| [**DWRITE \_ \_ MÉTRICAS DE SOBREGRAVAÇÕES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica quanto os DIPs visíveis (pixels independentes do dispositivo) sobrepõe cada lado do layout ou objetos em linha. |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | A [**união \_ PANOSE DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) descreve os valores de classificação de face de tipo que você usa com [**IDWriteFont1::GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) para selecionar e corresponder à fonte. |
| [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Armazena a associação de texto e seu script de sistema de escrita, bem como alguns atributos de exibição. |
| [**PROPRIEDADES DO SCRIPT DWRITE \_ \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | A [**estrutura DWRITE \_ SCRIPT \_ PROPERTIES**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) especifica as propriedades de script para navegação e justificativa do caret. |
| [**PROPRIEDADES DE \_ GLIFO DE \_ \_ FORMATAÇÃO DE DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contém propriedades de saída de formatação para um glifo de saída. |
| [**DWRITE \_ FORMATANDO \_ PROPRIEDADES DE \_ TEXTO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Modelando propriedades de saída para um glifo de saída. |
| [**TACHADO DE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contém informações sobre o tamanho e o posicionamento de tachões. |
| [**DWRITE \_ TEXT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contém as métricas associadas ao texto após o layout. |
| [**DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contém as métricas associadas ao texto após o layout. |
| [**INTERVALO DE TEXTO \_ \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Especifica um intervalo de posições de texto em que o formato é aplicado no texto representado por [**um objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) |
| [**DWRITE \_ TRIMMING**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Especifica a opção de corte para texto que estoura a caixa de layout.  |
| [**DWRITE \_ RECURSOS \_ TIPOGRÁFICOS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contém um conjunto de recursos tipográficos a serem aplicados durante a formatação de texto. |
| [**SUBLINHADO \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contém informações sobre a largura, a espessura, o deslocamento, a altura da corrida, a direção de leitura e a direção do fluxo de um sublinhado.  |
| [**DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | A [**estrutura DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) especifica o intervalo de pontos de código Unicode. |



 

