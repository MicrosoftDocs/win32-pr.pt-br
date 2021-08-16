---
title: Direct2D Glossário
description: descreve os termos comumente usados pela documentação do Direct2D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e884390-56e4-45ae-b1c9-c58503d6f2dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6102dc3ab10e48e5373bff2bcbe5e13ae3ca49a59417f05aae45d2106e0a3e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825626"
---
# <a name="direct2d-glossary"></a>Direct2D Glossário

<dl> <dt>

<span id="direct2d.direct2d_glossary_a8_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_A8_TARGET"></span>**Destino a8**
</dt> <dd>

Um destino de renderização que usa um formato de pixel que representa um canal alfa com oito bits. Os destinos A8 são úteis para desenhar geometrias como máscaras.

</dd> <dt>

<span id="direct2d.direct2d_glossary_aliasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ALIASING"></span>**alias**
</dt> <dd>

Em gráficos de computador, a aparência irregular de curvas ou linhas diagonais. A alias é mais visível em resoluções mais baixas.

</dd> <dt>

<span id="direct2d.direct2d_glossary_antialiasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ANTIALIASING"></span>**suavização**
</dt> <dd>

Uma técnica para suavizar a aparência irregular de linhas curvas ou diagonais. Os métodos de suavização incluem pixels circundantes com tons intermediários e manipulação do tamanho e alinhamento horizontal dos pixels.

</dd> <dt>

<span id="direct2d.direct2d_glossary_batch"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BATCH"></span>**lote**
</dt> <dd>

Um conjunto de solicitações ou transações que foram agrupadas.

</dd> <dt>

<span id="direct2d.direct2d_glossary_bitmap"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITMAP"></span>**bitmap**
</dt> <dd>

Uma representação de caracteres ou gráficos por pixels individuais. Os pixels podem ser organizados horizontalmente, em linhas ou verticalmente, em colunas. Cada pixel pode ser representado por um ou mais bits.

</dd> <dt>

<span id="direct2d.direct2d_glossary_bits_per_pixel__bpp_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITS_PER_PIXEL__BPP_"></span>**bits por pixel (BPP)**
</dt> <dd>

O número de bits que são usados para armazenar e exibir os dados de cor de um único pixel. Esta é a unidade padrão de medida para profundidade de bits (também chamada de profundidade de cor). As profundidades de bits comuns incluem 8, 16 e 32.

</dd> <dt>

<span id="direct2d.direct2d_glossary_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BRUSH"></span>**pincel**
</dt> <dd>

um recurso Direct2D que pinta um plano infinito com uma cor sólida, um gradiente ou um bitmap. Um pincel é normalmente usado para traçar e preencher uma geometria.

</dd> <dt>

<span id="direct2d.direct2d_glossary_cleartype"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_CLEARTYPE"></span>**ClearType**
</dt> <dd>

Uma tecnologia de exibição de fontes que melhora drasticamente a resolução da exibição da fonte, de modo que as letras na tela do computador pareçam suaves, não denteadas. O ClearType melhora a aparência do texto nos monitores LCD que têm uma interface digital, como monitores de laptop e monitores de desktop de tela plana de alta qualidade.

</dd> <dt>

<span id="direct2d.direct2d_glossary_dc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DC"></span>**ORIGEM**
</dt> <dd>

Consulte definição para: contexto do dispositivo.

</dd> <dt>

<span id="direct2d.direct2d_glossary_device_context__dc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DEVICE_CONTEXT__DC_"></span>**contexto do dispositivo (DC)**
</dt> <dd>

Um contexto de dispositivo GDI. Consulte também: Graphics Device Interface.

</dd> <dt>

<span id="direct2d.direct2d_glossary_direct2d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT2D"></span>**Direct2D**
</dt> <dd>

Uma API de renderização com aceleração de hardware e modo imediato de 2-D.

</dd> <dt>

<span id="direct2d.direct2d_glossary_direct3d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT3D"></span>**Avalia**
</dt> <dd>

A plataforma de aceleração de hardware e tempo de execução para gráficos 3D em Windows.

</dd> <dt>

<span id="direct2d.direct2d_glossary_directwrite"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTWRITE"></span>**DirectWrite**
</dt> <dd>

Uma API de texto que fornece processamento de texto, gerenciamento de fontes e suporte a layout de texto que é independente de qualquer sistema de renderização específico.

</dd> <dt>

<span id="direct2d.direct2d_glossary_directx_graphics_infrastructure__dxgi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTX_GRAPHICS_INFRASTRUCTURE__DXGI_"></span>**DXGI (infraestrutura gráfica do DirectX)**
</dt> <dd>

A infraestrutura que gerencia as tarefas relacionadas a elementos gráficos de baixo nível que são independentes do tempo de execução de gráficos do DirectX. DXGI fornece uma estrutura comum para componentes gráficos.

</dd> <dt>

<span id="direct2d.direct2d_glossary_dxgi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DXGI"></span>**DXGI**
</dt> <dd>

Consulte definição de: DXGI (infra-estrutura de gráficos do DirectX).

</dd> <dt>

<span id="direct2d.direct2d_glossary_figure"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FIGURE"></span>**figuras**
</dt> <dd>

Uma forma aberta ou fechada definida por um ponto inicial e uma coleção de segmentos.

</dd> <dt>

<span id="direct2d.direct2d_glossary_flatten"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FLATTEN"></span>**Dimensiona**
</dt> <dd>

Para gerar uma aproximação poligonal de uma geometria (potencialmente curva).

</dd> <dt>

<span id="direct2d.direct2d_glossary_gdi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GDI"></span>**GRÁFICA**
</dt> <dd>

Consulte definição para: Graphics Device Interface (GDI).

</dd> <dt>

<span id="direct2d.direct2d_glossary_geometric_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRIC_MASK"></span>**máscara geométrica**
</dt> <dd>

Um clipe ou um recorte, definido por um objeto ID2D1Geometry, que mascara uma camada quando é desenhado por um destino de renderização. Uma máscara geométrica pode ter um alias ou ter bordas de subpixel.

</dd> <dt>

<span id="direct2d.direct2d_glossary_geometry_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRY_TRANSFORM"></span>**transformação de geometria**
</dt> <dd>

Uma transformação que é aplicada a uma geometria antes de ser traçada ou preenchida.

</dd> <dt>

<span id="direct2d.direct2d_glossary_glyph"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH"></span>**ícones**
</dt> <dd>

Uma representação gráfica de um caractere, parte de um caractere ou uma sequência de caracteres.

</dd> <dt>

<span id="direct2d.direct2d_glossary_glyph_run"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH_RUN"></span>**execução de glifo**
</dt> <dd>

Uma execução contínua de glifos que compartilham um formato comum.

</dd> <dt>

<span id="direct2d.direct2d_glossary_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_BRUSH"></span>**pincel de gradiente**
</dt> <dd>

Um pincel que pinta uma área em uma progressão gradual de uma cor para outra ou de um sombreamento para outro sombreamento da mesma cor.

</dd> <dt>

<span id="direct2d.direct2d_glossary_gradient_stop"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_STOP"></span>**parada de gradiente**
</dt> <dd>

Uma cor específica que é definida para um local dentro da região de gradiente. As paradas de gradiente são usadas para definir a cor em locais específicos ao longo do caminho do gradiente.

</dd> <dt>

<span id="direct2d.direct2d_glossary_grahics_primitive"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAHICS_PRIMITIVE"></span>**Grahics primitivo**
</dt> <dd>

Em gráficos de computador, uma forma como uma linha, um círculo, uma curva ou um polígono que um adaptador gráfico pode desenhar, armazenar e manipular como uma entidade discreta.

</dd> <dt>

<span id="direct2d.direct2d_glossary_graphics_device_interface__gdi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAPHICS_DEVICE_INTERFACE__GDI_"></span>**Graphics Device Interface (GDI)**
</dt> <dd>

Uma API de gráficos que permite que os aplicativos enviem comandos gráficos para um dispositivo de exibição ou impressão, geralmente sem considerar suas especificações ou recursos. Um GDI do Microsoft Win32 recebe solicitações de renderização de aplicativos e passa essas solicitações para o GDI do modo kernel.

</dd> <dt>

<span id="direct2d.direct2d_glossary_handle_to_a_device_context__hdc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HANDLE_TO_A_DEVICE_CONTEXT__HDC_"></span>**identificador para um contexto de dispositivo (HDC)**
</dt> <dd>

Uma referência a um contexto de dispositivo GDI.

</dd> <dt>

<span id="direct2d.direct2d_glossary_hdc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HDC"></span>**HDC**
</dt> <dd>

Consulte a definição de: identificador para um contexto de dispositivo.

</dd> <dt>

<span id="direct2d.direct2d_glossary_mesh"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MESH"></span>**integrada**
</dt> <dd>

Uma coleção de vértices que definem um conjunto de triângulos que constituem uma forma.

</dd> <dt>

<span id="direct2d.direct2d_glossary_multi-sample_anti-aliasing__msaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MULTI-SAMPLE_ANTI-ALIASING__MSAA_"></span>**Multialiasing de várias amostras (MSAA)**
</dt> <dd>

Uma técnica de suavização que processa uma cena inteira.

</dd> <dt>

<span id="direct2d.direct2d_glossary_opacity_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_OPACITY_MASK"></span>**máscara de opacidade**
</dt> <dd>

Uma máscara, descrita por um pincel ou bitmap, que é aplicada a outro objeto para tornar esse objeto parcial ou completamente transparente. Uma máscara de opacidade usa informações de canal alfa para especificar como os pixels de origem do objeto são mesclados no destino final de destino. As partes transparentes da máscara indicam as áreas em que a imagem subjacente está oculta, enquanto as partes opacas da máscara indicam onde o objeto mascarado é permitido.

</dd> <dt>

<span id="direct2d.direct2d_glossary_per_primitive_anti-aliasing__ppaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_PER_PRIMITIVE_ANTI-ALIASING__PPAA_"></span>**PPAA (suavização de serrilhamento por primitiva)**
</dt> <dd>

Uma técnica de anti-aliasing que é aplicada a cada primitivo gráfico individual, em vez de uma cena inteira.

</dd> <dt>

<span id="direct2d.direct2d_glossary_radial_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RADIAL_GRADIENT_BRUSH"></span>**pincel de gradiente radial**
</dt> <dd>

Um gradiente em que o ponto inicial é definido por um ponto focal e o ponto final é definido por um gradiente.

</dd> <dt>

<span id="direct2d.direct2d_glossary_render_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RENDER_TARGET"></span>**destino de renderização**
</dt> <dd>

um recurso Direct2D que emite comandos de desenho. Há diferentes tipos de destinos de renderização, cada renderização em um destino diferente. Por exemplo, um ID2D1HwndRenderTarget é renderizado em uma janela e um ID2D1BitmapRenderTarget renderiza para um bitmap.

</dd> <dt>

<span id="direct2d.direct2d_glossary_segment"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_SEGMENT"></span>**explica**
</dt> <dd>

Uma parte de um caminho geométrico, definida pelos pontos inicial e final.

</dd> <dt>

<span id="direct2d.direct2d_glossary_tessellate"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TESSELLATE"></span>**incluí**
</dt> <dd>

Para dividir uma forma em uma coleção de triângulos.

</dd> <dt>

<span id="direct2d.direct2d_glossary_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSFORM"></span>**tenha**
</dt> <dd>

Uma matriz que representa um mapeamento linear em várias dimensões. Direct2D usa uma matriz 2-por-3, que limita a API a essas deformações que são afim.

</dd> <dt>

<span id="direct2d.direct2d_glossary_translation"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSLATION"></span>**transferência**
</dt> <dd>

O processo de usar uma matriz de transformação para mover um objeto.

</dd> <dt>

<span id="direct2d.direct2d_glossary_vertex"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX"></span>**deles**
</dt> <dd>

O ponto mais alto de uma curva, o ponto em que uma curva termina ou o ponto em que dois segmentos se encontram em um polígono ou em um caminho de forma livre.

</dd> <dt>

<span id="direct2d.direct2d_glossary_vertex_shader"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX_SHADER"></span>**sombreador de vértice**
</dt> <dd>

Um tipo de sombreador programável que contém um conjunto de instruções de assembly que são executados na GPU por vértice e por pixel para a chamada de desenho atual. Um sombreador de vértice descarrega cálculos intensivos da CPU para a GPU.

</dd> <dt>

<span id="direct2d.direct2d_glossary_windows_imaging_component__wic_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_WINDOWS_IMAGING_COMPONENT__WIC_"></span>**Windows Componente de imagens (WIC)**
</dt> <dd>

Uma API que permite que os aplicativos (1) exibem e editem qualquer formato de imagem para o qual um CODEC compatível com WIC está instalado e para (2) ler e gravar metadados ou arquivos de imagem.

</dd> <dt>

<span id="direct2d.direct2d_glossary_xml_paper_specification__xps_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XML_PAPER_SPECIFICATION__XPS_"></span>**XML Paper Specification (XPS)**
</dt> <dd>

Um formato de documento, descrito pela XML Paper Specification, que pode ser usado para armazenar documentos, processá-los para impressão e imprimi-los.

</dd> <dt>

<span id="direct2d.direct2d_glossary_xps"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XPS"></span>**Xps**
</dt> <dd>

Consulte definição para: XML Paper Specification (XPS).

</dd> </dl>

 

 




