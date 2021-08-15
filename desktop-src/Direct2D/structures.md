---
title: estruturas de Direct2D
description: Direct2D fornece as estruturas a seguir. Estruturas adicionais são definidas no namespace D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6be3735335abc5b9242ec150ac583f837ae5c15936aaca677b322526b1c19f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537696"
---
# <a name="direct2d-structures"></a>estruturas de Direct2D

Direct2D fornece as estruturas a seguir. Estruturas adicionais são definidas no [namespace D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**D2D \_ cor \_ F**](d2d-color-f.md) | Descreve os componentes vermelho, verde, azul e alfa de uma cor. |
| [**D2D \_ matriz \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Representa uma matriz 3 por 2. |
| [**D2D \_ matriz \_ 4x3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Descreve uma matriz de ponto flutuante de 4 por 3. |
| [**D2D \_ matriz \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Descreve uma matriz de ponto flutuante de 4 por 4. |
| [**D2D \_ matriz \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Descreve uma matriz de ponto flutuante de 5 por 4. |
| [**\_Ponto D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Representa um par de coordenadas x e y, expresso como valores de ponto flutuante, em espaço bidimensional. |
| [**D2D \_ Point \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | A \_ estrutura 2L do D2D Point \_ define as coordenadas x e y de um ponto. |
| [**D2D \_ ponto \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Representa um par de coordenadas x e y, expresso como um valor inteiro de 32 bits sem sinal, em espaço bidimensional. |
| [**D2D \_ Rect \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Representa um retângulo definido pelas coordenadas do canto superior esquerdo (esquerda, superior) e as coordenadas do canto inferior direito (direita, inferior).  |
| [**D2D \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | A [**estrutura \_ \_ L do D2D Rect**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) define as coordenadas dos cantos superior esquerdo e inferior direito de um retângulo. |
| [**D2D \_ Rect \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Representa um retângulo definido pelo par de coordenadas do canto superior esquerdo (esquerda, superior) e o par de coordenadas de canto inferior direito (direita, inferior). Essas coordenadas são expressas como valores inteiros de 32 bits. |
| [**D2D \_ tamanho \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Armazena um par ordenado de valores de ponto flutuante, normalmente a largura e a altura de um retângulo.  |
| [**D2D \_ tamanho \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo. |
| [**\_Vetor D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Um vetor 2D que consiste em dois valores de ponto flutuante de precisão simples (x, y).  |
| [**\_3F de vetor D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Um vetor 3D que consiste em três valores de ponto flutuante de precisão simples (x, y, z). |
| [**\_4F de vetor D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Um vetor 4D que consiste em quatro valores de ponto flutuante de precisão simples (x, y, z, w). |
| [**\_Segmento de arco d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Descreve um arco elíptico entre dois pontos. |
| [**\_Segmento de BEZIER d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Representa um segmento de Bezier cúbico desenhado entre dois pontos. |
| [**\_Propriedades do \_ pincel de bitmap d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Descreve os modos de extensão e o modo de interpolação de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_PROPERTIES1 de \_ pincel de bitmap d2d1 \_**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Descreve os modos de extensão e o modo de interpolação de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_Propriedades de bitmap d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Descreve o formato de pixel e dpi de um bitmap. |
| [**D2D1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Essa estrutura permite que um [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) seja criado com opções de bitmap e informações de contexto de cor disponíveis.  |
| [**\_Descrição da combinação de d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Define uma descrição de mistura a ser usada em uma transformação de mesclagem específica. |
| [**\_Propriedades do pincel d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Descreve a opacidade e a transformação de um pincel. |
| [**D2D1 \_ cor \_ F**](d2d1-color-f.md) | Descreve os componentes vermelho, verde, azul e alfa de uma cor. |
| [**\_Propriedades de criação de d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | especifica as opções com as quais o dispositivo [Direct2D](./direct2d-portal.md) , a fábrica e o contexto do dispositivo são criados.  |
| [**\_Propriedades do \_ buffer de vértice personalizado \_ do d2d1 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Define um sombreador de vértice e a descrição do elemento de entrada para definir o layout de entrada. |
| [**\_Descrição do \_ estado de desenho do d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Descreve o estado de desenho de um destino de renderização.  |
| [**\_DESCRIPTION1 do \_ estado de desenho d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Descreve o estado de desenho de um contexto de dispositivo. |
| [**\_Descrição da \_ entrada do efeito d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Descreve os recursos de um efeito. |
| [**\_Elipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Contém o ponto central, o x-raio e o raio y de uma elipse. |
| [**\_Opções de fábrica do d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Contém o nível de depuração de um objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .  |
| [**\_ \_ Duplos de dados de recurso d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Descreve o suporte para duplos em sombreadores. |
| [**D2D1 \_ recurso \_ dados \_ d3d10 \_ X \_ Opções de hardware \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Descreve o suporte ao sombreador de computação, que é uma opção no nível de recurso D3D10. |
| [**\_Patch de malha de gradiente d2d1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Representa um patch tensor com 16 pontos de controle, 4 cores de canto e sinalizadores de limite. Um ID2D1GradientMesh é composto por 1 ou mais patches de malha de gradiente. Use a [**função GradientMeshPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) ou a [**função GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) para criar uma.  |
| [**\_Parada de gradiente d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Contém a posição e a cor de uma parada de gradiente.  |
| [**\_Propriedades de \_ destino de renderização d2d1 HWND \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Contém as opções de HWND, tamanho de pixel e apresentação para um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget). |
| [**\_Propriedades de \_ estilo de tinta d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Define a forma da dica de caneta geral e a transformação usada em um objeto [**ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) .  |
| [**\_Propriedades do \_ pincel de imagem d2d1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Descreve os recursos de pincel de imagem. |
| [**\_Segmento de \_ BEZIER de tinta d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Representa um segmento de Bézier a ser usado na criação de um objeto [**ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) . Essa estrutura é diferente do [**\_ \_ segmento de BEZIER d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) , pois é composta por [**d2d1 \_ de \_ ponto de tinta**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point), que contêm um raio além das coordenadas x e y.  |
| [**\_Ponto de tinta d2d1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Representa um par de ponto, raio que faz parte de um [**\_ segmento de \_ BEZIER \_ de tinta d2d1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**\_Descrição de entrada do d2d1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Descreve as opções que as transformações podem definir em texturas de entrada. |
| [**\_Elemento de entrada d2d1 \_ \_ desc**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Uma descrição de um único elemento para o layout de vértice. |
| [**PARÂMETROS DE CAMADA D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Contém os limites de conteúdo, informações de máscara, configurações de opacidade e outras opções para um recurso de camada.  |
| [**D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Contém os limites de conteúdo, informações de máscara, configurações de opacidade e outras opções para um recurso de camada. |
| [**PROPRIEDADES DO PINCEL \_ DE \_ GRADIENTE LINEAR \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Contém o ponto de partida e o ponto de extremidade do eixo de gradiente para [**um ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)  |
| [**D2D1 \_ MATRIX \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | Representa uma matriz 3 por 2.  |
| [**D2D1 \_ MATRIX \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Representa uma matriz 4 por 3.  |
| [**D2D1 \_ MATRIX \_ 4X4 \_ F**](d2d1-matrix-4x4-f.md) | Representa uma matriz 4 por 4.  |
| [**D2D1 \_ MATRIX \_ 5X4 \_ F**](d2d1-matrix-5x4-f.md) | Representa uma matriz 5 por 4.  |
| [**D2D1 \_ \_ RECT MAPEADO**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Descreve a memória mapeada da [**API ID2D1Bitmap1::Map.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) |
| [**FORMATO DE PIXEL D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Contém o formato de dados e o modo alfa para um bitmap ou destino de renderização.  |
| [**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md) | Representa um par de coordenadas x e y no espaço bidimensional. |
| [**D2D1 \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | A estrutura POINT define as coordenadas x e y de um ponto. |
| [**D2D1 \_ POINT \_ 2U**](d2d1-point-2u.md) | Representa um par de coordenadas x e y no espaço bidimensional.  |
| [**D2D1 \_ POINT \_ DESCRIPTION**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Descreve um ponto em uma geometria de caminho. |
| [**PROPRIEDADES DO CONTROLE DE IMPRESSÃO D2D1 \_ \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | As propriedades de criação de [**um objeto ID2D1PrintControl.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) |
| [**ASSOCIAÇÃO DE PROPRIEDADE D2D1 \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Define uma associação de propriedade para um par de funções que obter e definir a propriedade correspondente.  |
| [**SEGMENTO DE \_ \_ BÉZIER QUADRÁTICO D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Contém o ponto de controle e o ponto de extremidade para um segmento de Bézier quadrático. |
| [**PROPRIEDADES DO PINCEL \_ DE \_ GRADIENTE RADIAL \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Contém o deslocamento de origem do gradiente e o tamanho e a posição da elipse de gradiente para [**um ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)  |
| [**D2D1 \_ RECT \_ F**](d2d1-rect-f.md) | Representa um retângulo definido pelas coordenadas do canto superior esquerdo (esquerda, superior) e as coordenadas do canto inferior direito (direita, inferior).  |
| [**D2D1 \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | A estrutura RECT define as coordenadas dos cantos superior esquerdo e inferior direito de um retângulo. |
| [**D2D1 \_ RECT \_ U**](d2d1-rect-u.md) | Representa um retângulo definido pelas coordenadas do canto superior esquerdo (esquerda, superior) e as coordenadas do canto inferior direito (direita, inferior).  |
| [**PROPRIEDADES DE TEXTURA DO RECURSO D2D1 \_ \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Define uma textura de recurso quando a textura do recurso original é criada. |
| [**USO DE RECURSOS D2D1 \_ \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Descreve a memória usada por texturas e sombreadores de imagem. |
| [**PROPRIEDADES DE DESTINO DE \_ \_ RENDERIZAÇÃO D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Contém opções de renderização (hardware ou software), formato de pixel, informações de DPI, opções de comunicação comunicação e requisitos de suporte do Direct3D para um destino de renderização.  |
| [**CONTROLES DE RENDERIZAÇÃO D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Descreve as limitações a serem aplicadas a um renderador de efeito de imagem. |
| [**D2D1 \_ \_ RECT ARREDONDADO**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Contém as dimensões e os raios de canto de um retângulo arredondado. |
| [**PERFIL DE COR SIMPLES D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Descrição simples de um espaço de cores. |
| [**D2D1 \_ TAMANHO \_ F**](d2d1-size-f.md) | Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo. |
| [**D2D1 \_ TAMANHO \_ U**](d2d1-size-u.md) | Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo. |
| [**PROPRIEDADES DE ESTILO DE TRAÇO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Descreve o traço que descreve uma forma.  |
| [**PROPRIEDADES DE ESTILO \_ DE TRAÇO D2D1111 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Descreve o traço que descreve uma forma. |
| [**COMPRIMENTO DO SVG D2D1 \_ \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Representa um comprimento SVG. |
| [**D2D1 \_ SVG \_ PRESERVAR TAXA DE \_ \_ PROPORÇÃO**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Representa todas as configurações de preserveAspectRatio do SVG. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Representa uma exibição SVGBox. |
| [**PROPRIEDADES DE ORIGEM DA \_ \_ IMAGEM TRANSFORMADA \_ D2D1 \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Propriedades de uma fonte de imagem transformada. |
| [**TRIÂNGULO D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Contém os três vértices que descrevem um triângulo. |
| [**D2D1 \_ VECTOR \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Um vetor de 2 valores FLOAT (x, y). |
| [**D2D1 \_ VECTOR \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Um vetor de 3 valores FLOAT (x, y, z). |
| [**D2D1 \_ VECTOR \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Um vetor de 4 valores FLOAT (x, y, z, w). |
| [**PROPRIEDADES DO \_ BUFFER DE VÉRTICE D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Define as propriedades de um buffer de vértice que são padrão para todas as definições de sombreador de vértice. |
| [**INTERVALO DE \_ VÉRTICE D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Define um intervalo de vértices que são usados ao renderizar menos que o conteúdo completo de um buffer de vértice. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Armazena informações de cor e canal alfa. |
| [*PD2D1 \_ EFFECT \_ FACTORY*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Descreve a implementação de um efeito. |