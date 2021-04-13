---
title: Estágio do assembler de entrada
description: A API do Direct3D 10 e superior separa áreas funcionais do pipeline em estágios; o primeiro estágio no pipeline é o estágio de IA (assembler de entrada).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- estágio do assembler de entrada (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368965"
---
# <a name="input-assembler-stage"></a>Estágio do assembler de entrada

A API do Direct3D 10 e superior separa áreas funcionais do pipeline em estágios; o primeiro estágio no pipeline é o estágio de IA (assembler de entrada).

A finalidade do estágio de montagem de entrada é ler dados primitivos (pontos, linhas e/ou triângulos) de buffers preenchidos pelo usuário e montar os dados em primitivos que serão usados por outros estágios de pipeline. O estágio de IA pode reunir vértices em vários [tipos primitivos](d3d10-graphics-programming-guide-primitive-topologies.md) diferentes (por exemplo, listas de linha, faixas de triângulos ou primitivas com adjacência). Novos tipos primitivos (como uma lista de linhas com adjacência ou uma lista de triângulos com adjacências) foram adicionados para dar suporte ao sombreador de geometria.

Informações de adjacência são visíveis para um app apenas em um sombreador de geometria. Se um sombreador de geometria for invocado com um triângulo incluindo adjacência, por exemplo, os dados de entrada conterão 3 vértices para cada triângulo e 3 vértices para dados de adjacência por triângulo.

Quando o estágio Input-Assembler é solicitado para gerar dados de adjacência, os dados de entrada devem incluir dados de adjacência. Isso pode exigir o fornecimento de um vértice fictício (formando um triângulo degenerado), ou talvez sinalização em um dos atributos de vértice, seja o vértice existente ou não. Isso também precisaria ser detectado e manipulado por um sombreador de geometria, embora a seleção da geometria degenerada aconteça no estágio de rasterizador.

Ao montar primitivos, uma finalidade secundária do IA é anexar [valores gerados pelo sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) para ajudar a tornar os sombreadores mais eficientes. Valores gerados pelo sistema são cadeias de caracteres de texto que também são chamadas de semântica. Todos os três estágios de sombreador são construídos a partir de um núcleo de sombreador comum, e o sombreador Core usa valores gerados pelo sistema (como uma ID primitiva, uma ID de instância ou uma ID de vértice) para que um estágio de sombreador possa reduzir o processamento apenas para os primitivos, instâncias ou vértices que ainda não foram processados.

Conforme mostrado no [diagrama de bloco de pipeline](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), quando o estágio ia lê dados da memória (monta os dados em primitivos e anexa valores gerados pelo sistema), os dados são impressos no estágio do [sombreador de vértice](/previous-versions//bb205146(v=vs.85)).


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução com o estágio de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Há algumas etapas necessárias para inicializar o estágio de IA (assembler de entrada). Por exemplo, você precisa criar recursos de buffer com os dados de vértice que o pipeline precisa, dizer ao estágio IA onde estão os buffers e que tipo de dados eles contêm, e especificar o tipo de primitivas a serem montadas dos dados.<br/> |
| [Topologias primitivas](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | O Direct3D 10 e superior dá suporte a vários tipos primitivos (ou topologias) que são representados pelo tipo enumerado da [**\_ \_ topologia primitiva do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Esses tipos definem como os vértices são interpretados e renderizados pelo pipeline.<br/>                                                          |
| [Usando o estágio de Input-Assembler sem buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | A criação e a associação de buffers não são necessárias se os sombreadores não exigem buffers. Esta seção contém um exemplo de vértice simples e sombreadores de pixel que desenham um único triângulo.<br/>                                                                                                                                  |
| [Usando valores de System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Os valores gerados pelo sistema são gerados pelo estágio IA (com base na [semântica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de entrada fornecida pelo usuário) para permitir determinadas eficiências em operações de sombreador. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

