---
title: Estruturas DirectWrite
description: DirectWrite define as estruturas a seguir.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea132cde1ea6b740cc02b938767f941e9c999e5a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105789820"
---
# <a name="directwrite-structures"></a>Estruturas DirectWrite

DirectWrite define as estruturas a seguir.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md) | Representa dados de bitmap no formato BGRA32. |
| [**\_métricas de cursor DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | A estrutura de [**\_ \_ métricas de cursor DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) especifica as métricas para o posicionamento do cursor em uma fonte. |
| [**\_métricas de cluster DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contém informações sobre um cluster de glifos. |
| [**DWRITE \_ cor \_ F**](dwrite-color-f.md) | Descreve os componentes vermelho, verde, azul e alfa de uma cor. |
| [**\_execução de \_ glifo de cor DWRITE \_**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contém as informações necessárias para os renderizadores para desenhar as execuções de glifos com informações de cor de glifo. |
| [**\_RUN1 de \_ glifo de cor DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Representa uma execução de glifo de cor. O método IDWriteFactory4:: TranslateColorGlyphRun retorna uma coleção ordenada de execuções de glifos de cores de tipos variados, dependendo do suporte da fonte. |
| [**\_fragmento de arquivo DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Representa um intervalo de bytes em um arquivo de fonte. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Representa o intervalo mínimo e máximo dos valores possíveis para um eixo de fonte. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Representa um valor para um eixo de fonte. Usado ao consultar e criar instâncias de fonte. |
| [**\_recurso fonte \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Especifica as propriedades usadas para identificar e executar recursos tipográficos na face da fonte atual. |
| [**\_métricas de fonte DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | A estrutura de [**\_ \_ métricas de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) especifica as métricas que são aplicáveis a todos os glifos dentro da face da fonte. |
| [**DWRITE \_ Font \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | A [**estrutura \_ \_ METRICS1 da fonte DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) especifica as métricas que são aplicáveis a todos os glifos dentro da face da fonte. |
| [**\_propriedade de fonte DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Propriedade Font usada para filtrar conjuntos de fontes e criar um conjunto de fontes com propriedades explícitas. |
| [**\_dados de \_ imagem de glifo DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Dados para um único glifo de GetGlyphImageData. |
| [**\_métricas de GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Especifica as métricas de um glifo individual. |
| [**\_deslocamento de GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | O ajuste opcional para a posição de um glifo. |
| [**\_execução de GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contém as informações necessárias para os renderizadores para desenhar execuções de glifo. |
| [**\_Descrição da \_ execução de glifo DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contém propriedades adicionais relacionadas àquelas na [**\_ \_ execução de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_ \_ métricas de teste de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Descreve a região obtida por um teste de clique. |
| [**\_ \_ métricas de objeto EMBUTIdo DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contém propriedades que descrevem a medição geométrica de um objeto embutido definido pelo aplicativo. |
| [**\_oportunidade de justificação de DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | A estrutura de [**\_ \_ oportunidade de justificação de DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) especifica informações de justificativa por glifo. |
| [**ponto de interrupção de \_ linha DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Características de ponto de interrupção de linha de um caractere. |
| [**\_métricas de linha de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contém informações sobre uma linha de texto formatada. |
| [**DWRITE \_ linha \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contém informações sobre uma linha de texto formatada. |
| [**\_espaçamento de linha DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | A estrutura da [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) especifica a transformação de gráficos a ser aplicada aos glifos renderizados. |
| [**\_métricas de folga DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica quanto de qualquer DIPs visível (pixels independentes de dispositivo) excede cada lado do layout ou dos objetos embutidos. |
| [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | A União [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) descreve os valores de classificação de tipo que você usa com [**IDWriteFont1:: getpanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) para selecionar e corresponder à fonte. |
| [**\_análise de script DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Armazena a associação de texto e seu script do sistema de escrita, bem como alguns atributos de exibição. |
| [**\_Propriedades do script DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | A estrutura de [**\_ \_ Propriedades de script DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) especifica as propriedades de script para navegação por cursor e justificativa. |
| [**\_Propriedades de \_ glifo de SHAPING de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contém propriedades de saída de formato para um glifo de saída. |
| [**\_Propriedades de \_ texto de SHAPING de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Formatar Propriedades de saída para um glifo de saída. |
| [**DWRITE \_ tachado**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contém informações sobre o tamanho e o posicionamento de tachados. |
| [**\_métricas de texto DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contém as métricas associadas ao layout de texto após. |
| [**\_METRICS1 de texto DWRITE \_**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contém as métricas associadas ao layout de texto após. |
| [**\_intervalo de texto DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Especifica um intervalo de posições de texto em que o formato é aplicado no texto representado por um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . |
| [**\_corte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Especifica a opção de corte para o estouro de texto da caixa de layout.  |
| [**\_recursos tipográficos do DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contém um conjunto de recursos tipográficos a serem aplicados durante o Shaping de texto. |
| [**\_sublinhado DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contém informações sobre a largura, a espessura, o deslocamento, a altura da execução, a direção da leitura e a direção do fluxo de um sublinhado.  |
| [**intervalo de DWRITE \_ Unicode \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | A estrutura de [**\_ \_ intervalo do DWRITE Unicode**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) especifica o intervalo de pontos de código Unicode. |



 

