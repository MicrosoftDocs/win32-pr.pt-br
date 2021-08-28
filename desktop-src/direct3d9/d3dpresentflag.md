---
description: Constantes usadas por \_ PARÂMETROS D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf3a8ad3a22f5104e4d4a78d3a01a29d07d757
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624552"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Constantes usadas por [**\_ PARÂMETROS D3DPRESENT.**](d3dpresent-parameters.md)



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Valor</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit in the window client area, within the monitor screen area of the video adapter that created the Direct3D device. D3DPRESENTFLAG_DEVICECLIP não é válido com D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>De definir esse sinalizador quando o dispositivo ou a cadeia de permutas for criado para habilitar o descarte de buffer z. Se esse sinalizador for definido, o conteúdo do buffer de estêncil de profundidade será inválido depois de chamar <a href="/windows/desktop/api"><strong>Present</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> com uma superfície de profundidade diferente. Descartar dados de buffer z pode aumentar o desempenho e é dependente do driver. O runtime de depuração imporá o descarte limpando o buffer z para algum valor constante depois de chamar <a href="/windows/desktop/api"><strong>Present</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> com uma superfície de profundidade diferente.<br/> Descartar dados de buffer z é ilegal para todos os formatos que podem ser D3DFMT_D16_LOCKABLE e D3DFMT_D32F_LOCKABLE. Qualquer uso de <a href="/windows/desktop/api"><strong>CreateDevice especificando</strong></a> um formato bloqueável e o descarte de buffer z falhará. Para obter mais informações sobre formatos, <a href="d3dformat.md">consulte D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>De definir esse sinalizador se o aplicativo exigir a capacidade de bloquear o buffer de fundo diretamente. Observe que os buffers de fundo não são bloqueiáveis, a menos que o aplicativo especifique D3DPRESENTFLAG_LOCKABLE_BACKBUFFER ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> ou <a href="/windows/desktop/api"><strong>Redefinir</strong></a>. Buffers de fundo com bloqueio incorrem em um custo de desempenho em algumas configurações de hardware de gráficos. Executar uma operação de bloqueio (ou usar <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> para gravar) no buffer de fundo com bloqueio diminui o desempenho em muitos cartões. Nesse caso, considere o uso de triângulos texturados para mover dados para o buffer de fundo.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> No Direct3D9Ex, esse sinalizador não poderá ser definido se o D3DSWAPEFFECT for D3DSWAPEFFECT_FLIPEX, pois o modelo de in flip permite que o Gerenciador de Janelas da Área de Trabalho acesse o buffer de back de um aplicativo. Uma superfície compartilhada entre processos não deve ser bloqueada.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Os monitores girados são tratados automaticamente com uma cópia giratória durante a apresentação, o que não é muito eficiente. Esse sinalizador significa que o aplicativo executará sua própria rotação de exibição. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Os aplicativos podem obter sua própria rotação possivelmente usando uma matriz de exibição girada. Os métodos <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> devem ser usados para encontrar a configuração de rotação atual. Os parâmetros Largura e Altura do backbuffer em <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> devem ser usar orientação paisagem, enquanto a estrutura do modo de exibição de tela inteira deve ser a mesma que é retornada de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (ou seja, Largura e Altura são trocadas quando giradas 90 e 270 graus).</p>
<p>Ao usar Bloquear em destinos de renderização girados, as suposições do canto superior esquerdo não se mantêm verdadeiras, o destino de renderização SURFACE_DESC permanecerá paisagem (conforme implícito nos parâmetros de criação) e a janela GDI, as coordenadas do mouse e essas precisam ser traduzidas corretamente quando usadas com o destino de renderização e a cena do Direct3D.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Use esse sinalizador para especificar qualquer modo de exibição RAW enumerado pelo adaptador de exibição, embora o Direct3D possa ter indicado que o modo é inválido. O aplicativo deve implementar isso de maneira robusta caso o modo desejado realmente seja inválido. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Essa é uma dica para o driver de que os buffers de fundo conterão dados de vídeo.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Especifica se a sobreposição é RGB de intervalo completo ou RGB de intervalo limitado. Definir esse sinalizador indica um intervalo limitado RGB. No intervalo limitado RGB, o intervalo RGB é compactado de forma que 16:16:16 seja preto e 235:235:235 seja branco.
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Especifica se a sobreposição é BT.601 ou BT.709. Definir esse sinalizador indica BT.709, para HDTV (TV de alta definição).
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Especifica se a sobreposição é YCbCr convencional ou YCbCr estendido (sempreYCC). Definir esse sinalizador indica YCbCr estendido (cbycc).
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>Definir esse sinalizador indica que a swapchain contém conteúdo protegido e faz com que o runtime restrinja automaticamente o acesso à swapchain para que apenas o DWM (Desktop Windows Manager) possa usar a swapchain.
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>Definir esse sinalizador indica que o driver deve restringir o acesso a todos os recursos compartilhados criados para interação DWM. O chamador deve criar um canal autenticado com o driver. Em seguida, o driver deve permitir o acesso a processos que tentam abrir esses recursos compartilhados.
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas [**por \_ PARÂMETROS D3DPRESENT.**](d3dpresent-parameters.md)

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3d9types.h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




