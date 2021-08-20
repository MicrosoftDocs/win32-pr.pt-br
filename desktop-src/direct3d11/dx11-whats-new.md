---
title: Novidades no SDK de agosto de 2009 Windows 7/Direct3D 11
description: Esta versão do Windows 7/Direct3D 11 é apresentada como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c51f350065134893ed2303d8854eb9d24fc7f58e8ab762f71da019d89d45b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608906"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Novidades no SDK de agosto de 2009 Windows 7/Direct3D 11

Esta versão do Windows 7/Direct3D 11 é apresentada como parte do SDK do DirectX e contém novos recursos, ferramentas e documentação.



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
<td>Direct2D é uma API de gráficos 2D acelerada por hardware e modo imediato que fornece renderização de alto desempenho e alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D é projetada para interoperar bem com Direct3D e GDI. Esse SDK permite que os desenvolvedores avaliem a API e escrevam aplicativos simples, com algumas das funcionalidades mais avançadas possíveis em máquinas configuradas corretamente. <br/> <a href="/windows/win32/direct2d/direct2d-portal">A</a> <a href="/previous-versions//dd372354(v=vs.85)">documentação e exemplos</a> Direct2D estão disponíveis atualmente no MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite fornece suporte para renderização de texto de alta qualidade, fontes de estrutura de contorno independentes de resolução, suporte completo a texto e layout Unicode e muito mais:<br/>
<ul>
<li>Um sistema de layout de texto independente de dispositivo que melhora a capacidade de leitura de texto em documentos e na interface do usuário.<br/></li>
<li>Renderização de texto ClearType de alta qualidade, sub pixel, que pode usar o GDI Direct3D, Direct2D ou tecnologia de renderização específica do aplicativo.<br/></li>
<li>Suporte para texto de vários formatos. <br/></li>
<li>Suporte para os recursos avançados de tipografia de fontes OpenType.<br/></li>
<li>Suporte para o layout e renderização de texto em todos os idiomas com suporte do Windows.<br/></li>
</ul>
Esse SDK permite que os desenvolvedores avaliem a API e escrevam aplicativos básicos apenas para fins de demonstração.<br/> <a href="/windows/win32/directwrite/direct-write-portal">A</a> <a href="/windows/win32/directwrite/samples">documentação e exemplos</a> DirectWrite estão disponíveis atualmente no MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">O DXGI 1.1</a> se baseia no DXGI 1.0 e estará disponível no Windows Vista e Windows 7. O DXGI 1.1 adiciona vários novos recursos:<br/>
<ul>
<li>Suporte a superfícies compartilhadas sincronizadas. Isso permite o compartilhamento eficiente de superfície de leitura e gravação entre vários dispositivos D3D (pode estar entre D3D10 e D3D11).<br/></li>
<li>Suporte ao formato BGRA. Isso permite que a GDI renderizar para a mesma superfície DXGI direcionada por um dispositivo Direct2D, Direct3D 10.1 ou Direct3D 11. <br/></li>
<li>Latência máxima do quadro. Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> e <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, os títulos podem controlar o número de quadros que têm permissão para serem armazenados em uma fila, antes do envio para renderização. A latência geralmente é usada para controlar como a CPU escolhe entre responder à entrada do usuário e quadros que estão na fila de renderização.<br/></li>
<li>Enumeração do adaptador. Usando <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, os títulos podem enumerar adaptadores locais sem monitores ou saídas anexadas, bem como adaptadores com saídas anexadas.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Exemplos atualizados<br/></td>
<td>Esta versão tem vários exemplos novos e atualizados.<br/>
<ul>
<li>O novo <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> é uma ilustração das técnicas mais avançadas de processamento do sombreador de computação que podem ser executados em uma GPU D3D10 ou D3D11.</li>
<li>O exemplo <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> foi expandido para implementar efeitos de desfoque e de desfoque (além do mapeamento de tom) usando o sombreador de computação, bem como fornecendo implementações de sombreador de pixel para comparação.</li>
<li>A <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">amostra MultithreadedRendering11</a> foi atualizada significativamente, com ativos de arte mais complexos e processamento por thread mais intensivo.</li>
<li>O <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">exemplo SubD11</a> foi atualizado com um novo modelo facial e agora o exemplo aproveita o recurso de computação de adjaciação do Exportador de Conteúdo de Exemplos.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos introduzidos em versões anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

