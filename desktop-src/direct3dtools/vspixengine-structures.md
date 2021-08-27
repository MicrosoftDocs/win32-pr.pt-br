---
description: As estruturas a seguir são declaradas em vspixengine.h.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estruturas de interface de captura de diagnóstico do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 611a8112c1eb99c142c92f63f598e903352528f8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622282"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Estruturas de interface de captura de diagnóstico do Direct3D

As estruturas a seguir são declaradas em vspixengine.h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Nesta seção

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Tópico</th><th>Descrição</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>Representa um recurso compartilhado codificado como uma cadeia de caracteres COM.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>Representa informações de heap do descritor.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>Representa um erro em um estágio de pipeline.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>Representa um estágio de pipeline, incluindo detalhes do sombreador usado.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>Representa informações de gatilho do experimento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>Representa um pacote de quatro chamadas.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>Representa informações sobre o servidor de símbolos de depuração.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>Representa informações sobre um quadro na callstack.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>Representa informações sobre um arquivo de código-fonte.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>Representa informações resumidas sobre um evento.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>Representa informações sobre um sombreador no depurador.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Experimento</strong></a></p></td><td><p>Representa informações sobre um experimento (captura).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Problema</strong></a></p></td><td><p>Representa informações sobre um problema.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2d</strong></a></p></td><td><p>Representa um ponto 2D com coordenadas de inteiro sem sinal.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Representa um índice 3D em dados de thread</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>Representa os campos de layout de entrada de um buffer de vértice, um por campo no buffer de vértice.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>Representa informações sobre o histórico de pixels.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>Representa informações sobre um determinado</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>Representa informações sobre uma única entrada no layout do buffer de uma malha.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>Representa informações sobre uma solicitação do depurador de sombreador.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PomEngineInt4</strong></a></p></td><td><p>Representa um vetor 4D com coordenadas de inteiro com sinal.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>EnginePoint4D</strong></a></p></td><td><p>Representa um ponto 4D com coordenadas de ponto flutuante de 64 bits (duplo).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>YorkEngineChannelDesc</strong></a></p></td><td><p>Representa uma descrição de um canal de cor (exemplo).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>YorkEngineTextureFormatDesc</strong></a></p></td><td><p>Representa uma descrição de um formato de textura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>EngineTextureDescriptor</strong></a></p></td><td><p>Representa uma descrição de um recurso de textura.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>EngineTextureSliceDescriptor</strong></a></p></td><td><p>Representa uma descrição de uma fatia de textura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>DexEngineTextureSliceIndex</strong></a></p></td><td><p>Representa o índice de uma fatia de textura</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>GramEngineHistogram</strong></a></p></td><td><p>Representa um histograma de uma textura.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Tópicos relacionados

[Referência da interface de captura de diagnóstico do Direct3D](vspixengine-reference.md)

 

 
