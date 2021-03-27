---
title: O que há de novo no SDK de agosto de 2009 do Windows 7/Direct3D 11
description: Esta versão do Windows 7/Direct3D 11 é fornecida como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642164"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>O que há de novo no SDK de agosto de 2009 do Windows 7/Direct3D 11

Esta versão do Windows 7/Direct3D 11 é fornecida como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>O Direct2D é uma API de gráficos 2D, de modo imediato e com aceleração de hardware que fornece alto desempenho e renderização de alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D foi projetada para interoperar bem com Direct3D e GDI. Esse SDK permite que os desenvolvedores avaliem a API e gravem aplicativos simples, com algumas das funcionalidades mais avançadas possíveis em computadores configurados corretamente. <br/> A <a href="/windows/win32/direct2d/direct2d-portal">documentação</a> e os <a href="/previous-versions//dd372354(v=vs.85)">exemplos</a> do Direct2D estão disponíveis no momento no msdn.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>O DirectWrite fornece suporte para renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução, suporte completo a texto e layout Unicode e muito mais:<br/>
<ul>
<li>Um sistema de layout de texto independente de dispositivo que melhora a legibilidade do texto em documentos e na interface do usuário.<br/></li>
<li>Renderização de texto ClearType de alta qualidade, sub-pixel, que pode usar tecnologia de renderização GDI Direct3D, Direct2D ou específica do aplicativo.<br/></li>
<li>Suporte para texto de vários formatos. <br/></li>
<li>Suporte para os recursos de tipografia avançada de fontes OpenType.<br/></li>
<li>Suporte para layout e renderização de texto em todos os idiomas com suporte no Windows.<br/></li>
</ul>
Esse SDK permite que os desenvolvedores avaliem a API e gravem aplicativos básicos apenas para fins de demonstração.<br/> A <a href="/windows/win32/directwrite/direct-write-portal">documentação</a> e os <a href="/windows/win32/directwrite/samples">exemplos</a> do DirectWrite estão disponíveis no momento no msdn.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td>O <a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">dxgi 1,1</a> se baseia em dxgi 1,0 e estará disponível no Windows Vista e no Windows 7. DXGI 1,1 adiciona vários recursos novos:<br/>
<ul>
<li>Suporte a superfícies compartilhadas. Isso permite o compartilhamento eficiente de superfície de leitura e gravação entre vários dispositivos D3D (podem estar entre D3D10 e D3D11).<br/></li>
<li>Suporte ao formato BGRA. Isso permite que o GDI seja renderizado na mesma superfície DXGI direcionada por um dispositivo Direct2D, Direct3D 10,1 ou Direct3D 11. <br/></li>
<li>Latência máxima do quadro. Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: GetMaximumFrameLatency</strong></a>, os títulos podem controlar o número de quadros que têm permissão para serem armazenados em uma fila, antes do envio para renderização. A latência é geralmente usada para controlar como a CPU escolhe entre responder a entradas de usuário e quadros que estão na fila de renderização.<br/></li>
<li>Enumeração de adaptador. Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>, os títulos podem enumerar adaptadores locais sem monitores ou saídas anexados, bem como adaptadores com saídas anexadas.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Amostras atualizadas<br/></td>
<td>Esta versão tem vários exemplos novos e atualizados.<br/>
<ul>
<li>O novo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> é uma ilustração de técnicas de processamento de sombreador de computação mais avançadas que podem ser executadas em uma GPU d3d10 ou D3D11.</li>
<li>O <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">exemplo de HDRToneMappingCS11</a> foi expandido para implementar efeitos de desfoque e flor (além de mapeamento de Tom) usando o sombreador de computação, bem como fornecer implementações de sombreador de pixel para comparação.</li>
<li>O <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">exemplo de MultithreadedRendering11</a> foi atualizado significativamente, com ativos de arte mais complexos e processamento por thread mais intensivo.</li>
<li>O <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">exemplo SubD11</a> foi atualizado com um novo modelo facial, e o exemplo agora aproveita o recurso de computação de proximidade do exportador de conteúdo de exemplos.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos introduzidos em versões anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

