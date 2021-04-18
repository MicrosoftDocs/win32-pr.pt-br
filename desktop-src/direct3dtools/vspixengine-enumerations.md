---
description: As enumerações a seguir são declaradas em vspixengine. h.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerações de interface de captura de diagnóstico Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 059f91aa806afd60d5efe755d015495eb2f445f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789528"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Enumerações de interface de captura de diagnóstico Direct3D

As enumerações a seguir são declaradas em vspixengine. h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Nesta seção

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Tópico</th><th>Descrição</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>IDs de cadeia de caracteres de recurso definidas pelo chamador a serem retornadas em dados XML para visualização de objetos</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Define as IDs de recurso para recursos de cadeia de caracteres compartilhada. Eles são passados para o mecanismo de captura do host. Eles são usados para exibir cadeias de caracteres para a sobreposição de HUD do aplicativo que está sendo capturado ou para passar valores de registro das opções do Visual Studio para o Engi de captura</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Resultado</strong></a></p></td><td><p>Valores de HRESULT personalizados para a interface de captura de diagnóstico de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>Uma enumeração usada para se comunicar entre o mecanismo de captura e um host (como o Visual Studio Diagnóstico de Gráficos).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>Uma enumeração usada para se comunicar entre o mecanismo de captura e um host (como o Visual Studio Diagnóstico de Gráficos).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixPipeResponse</strong></a></p></td><td><p>Uma enumeração usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>Uma enumeração usada para indicar qual versão do protocul de comunicação remota está sendo usada.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>Uma enumeração usada para indicar por que um pixel foi rejeitado.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>Um enum que contém sinalizadores usados para descrever um resultado de histórico de pixel. Consulte PixelHistoryOperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>Uma enumeração usada para indicar IDs de coluna bem conhecidas; Essas são IDs de coluna às quais todas as implementações devem dar suporte.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>Objectstatetype</strong></a></p></td><td><p>Interna</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>Uma enumeração usada para indicar as propriedades dos dados retornados de uma solicitação de tabela de objeto. Para obter mais informações, consulte IObjectTableRequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>PIPELINESTAGES</strong></a></p></td><td><p>Uma enumeração usada para indicar um estágio do pipeline de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>Uma enumeração usada para indicar o algoritmo de soma de verificação a ser usado.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EVENTTYPE</strong></a></p></td><td><p>Uma enumeração usada para indicar o tipo de um evento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Uma enumeração usada para indicar um cabeçalho coumn no Visualizador de heap do descritor</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Uma enumeração usada para indicar uma coluna no Visualizador de heap do descritor.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTOtype</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>Uma enumeração usada para indicar que tipo de buffer IGenericBufferDataRequest retorna.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Interna</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Uma enumeração usada para indicar a topologia de uma malha. Consulte MeshDataVertCallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>Uma enumeração usada para indicar os estágios de progresso na análise de quadros.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>Uma enumeração usada para indicar a fonte de informações gráficas para análise de quadros.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Tópicos relacionados

[Referência da interface de captura de diagnóstico do Direct3D](vspixengine-reference.md)

 

 
