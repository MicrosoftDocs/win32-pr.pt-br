---
title: Interfaces principais do Direct3D 11
description: Esta seção contém informações sobre as interfaces principais.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104454417"
---
# <a name="direct3d-11-core-interfaces"></a>Interfaces principais do Direct3D 11

Esta seção contém informações sobre as interfaces principais.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br/></td>
<td>Essa interface encapsula métodos para recuperar dados da GPU de forma assíncrona.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br/></td>
<td>A interface de estado de mesclagem contém uma descrição para o estado de mesclagem que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br/></td>
<td>A interface de estado de mesclagem contém uma descrição para o estado de mesclagem que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>. Essa interface de estado de mesclagem dá suporte a operações lógicas, bem como operações de mesclagem.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br/></td>
<td>A interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsula uma lista de comandos gráficos para reproduzir.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br/></td>
<td>Essa interface encapsula métodos para medir o desempenho da GPU.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br/></td>
<td>A interface de estado de estêncil de profundidade contém uma descrição para o estado de estêncil de profundidade que você pode associar ao <a href="d3d10-graphics-programming-guide-output-merger-stage.md">estágio de mesclagem de saída</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos. O <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos. O <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos. O <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos. O <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, como <strong>RegisterDeviceRemovedEvent</strong> e <strong>UnregisterDeviceRemoved</strong>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br/></td>
<td>A interface do dispositivo representa um adaptador virtual; Ele é usado para criar recursos. O <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br/></td>
<td>Uma interface de dispositivo-filho acessa dados usados por um dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br/></td>
<td>A interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> representa um contexto de dispositivo que gera comandos de renderização.<br/>
<blockquote>
[!Note]<br />
A versão mais recente dessa interface é <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduzida na atualização do Windows 10 para criadores. Aplicativos voltados atualização do Windows 10 para criadores deve usar a interface <strong>ID3D11DeviceContext4</strong> em vez de <strong>ID3D11Device</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br/></td>
<td>A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos. O <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br/></td>
<td>A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos. O <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br/></td>
<td>A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos. O <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br/></td>
<td>A interface de contexto do dispositivo representa um contexto de dispositivo; Ele é usado para renderizar comandos. O <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adiciona novos métodos a eles no <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br/></td>
<td>A interface <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> representa um objeto de estado de contexto, que contém informações de estado e comportamento sobre um dispositivo Microsoft Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br/></td>
<td>Representa um limite, um objeto usado para sincronização da CPU e uma ou mais GPUs.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br/></td>
<td>Uma interface de layout de entrada contém uma definição de como alimentar dados de vértice que são dispostos na memória no <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">estágio de Assembler de entrada</a> do <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline de gráficos</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br/></td>
<td>Fornece proteção de threading para seções críticas de um aplicativo multi-threaded.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br/></td>
<td>Uma interface de predicado determina se a geometria deve ser processada dependendo dos resultados de uma chamada de desenho anterior.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br/></td>
<td>Uma interface de consulta consulta informações da GPU.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br/></td>
<td>Representa um objeto de consulta para consultar informações da GPU (unidade de processamento gráfico).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br/></td>
<td>A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br/></td>
<td>A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>. Essa interface de estado do rasterizador dá suporte à contagem de amostra forçada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br/></td>
<td>A interface de estado do rasterizador contém uma descrição para o estado do rasterizador que você pode associar ao <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">estágio do rasterizador</a>. Essa interface de estado do rasterizador dá suporte à contagem de amostras forçada e ao modo de rasterização conservador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br/></td>
<td>A interface de estado de amostra contém uma descrição para o estado de amostra que você pode associar a qualquer estágio de sombreador do <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> para referência por operações de exemplo de textura.<br/></td>
</tr>
</tbody>
</table>



 

O Direct3D 11 implementa interfaces para:

-   [Recursos](d3d11-graphics-reference-resource-interfaces.md)
-   [Sombreadores](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência principal](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

