---
description: Consulte uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo na constante D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011279"
---
# <a name="d3dcreate"></a>D3DCREATE

Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definir</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>O aplicativo solicita que o dispositivo conduza todos os cabeçotes que esse adaptador mestre possui. O sinalizador é inválido em adaptadores não mestres. Se esse sinalizador for definido, os parâmetros de apresentação passados para <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> deverão apontar para uma matriz de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>. O número de elementos em <strong>D3DPRESENT_PARAMETERS</strong> deve ser igual ao número de adaptadores definidos pelo membro NumberOfAdaptersInGroup da estrutura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> . O tempo de execução do DirectX atribuirá cada elemento a cada cabeçalho na ordem numérica especificada pelo membro AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>O Direct3D gerenciará recursos em vez do driver. As chamadas Direct3D não falharão para erros de recurso, como memória de vídeo insuficiente.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Como D3DCREATE_DISABLE_DRIVER_MANAGEMENT, o Direct3D gerenciará os recursos em vez do driver. Ao contrário de D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX retornará erros para condições como memória de vídeo insuficiente.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Faz com que o tempo de execução não Registre as teclas de captura para a tela, Ctrl-Printscreen e Alt-Printscreen para capturar o conteúdo da área de trabalho ou da janela. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Restrinja a computação ao thread do aplicativo principal. Se o sinalizador não estiver definido, o tempo de execução poderá executar o processamento de vértice de software e outros cálculos no thread de trabalho para melhorar o desempenho em sistemas com vários processadores. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Windows XP e o Windows Vista:<br/> Esse sinalizador está disponível no Windows Vista, no Windows Server 2008 e no Windows 7.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Habilita a coleta de estatísticas atuais no dispositivo. Chamadas para <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> retornarão dados válidos. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Defina a precisão para cálculos de ponto flutuante do Direct3D para a precisão usada pelo thread de chamada. Se você não especificar esse sinalizador, o Direct3D usa como padrão o modo de ida e volta de precisão simples por dois motivos:
<ul>
<li>O modo de precisão dupla reduzirá o desempenho do Direct3D.</li>
<li>Partes do Direct3D pressupõem que as exceções de unidade de ponto flutuante são mascaradas; a remoção de máscara dessas exceções pode resultar em um comportamento indefinido.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Especifica o processamento de vértice de hardware.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Especifica o processamento de vértice misto (software e hardware). Para o Windows 10, versão 1607 e posterior, não é recomendável usar essa configuração. Consulte D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Especifica o processamento de vértice de software. Para o Windows 10, versão 1607 e posterior, não é recomendável usar essa configuração. Use D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
A menos que o processamento de vértice de hardware não esteja disponível, o uso do processamento de vértice de software não é recomendado no Windows 10, versão 1607 (e versões posteriores) porque a eficiência do processamento de vértice de software foi significativamente reduzida e, ao mesmo tempo, melhora a segurança da implementação.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indica que o aplicativo solicita que o Direct3D seja multithread seguro. Isso faz com que um thread Direct3D assuma a propriedade de sua <a href="/windows/desktop/Sync/critical-section-objects">seção crítica</a> global com mais frequência, o que pode prejudicar o desempenho. Se um aplicativo processar mensagens de janela em um thread ao fazer chamadas de API do Direct3D em outro, o aplicativo deverá usar esse sinalizador ao criar o dispositivo. Essa janela também deve ser destruída antes de descarregar d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indica que o Direct3D não deve alterar a janela de foco de forma alguma.
<div class="alert">
<blockquote>
[!Note]<br />
Se esse sinalizador for definido, o aplicativo deverá oferecer suporte total a todos os eventos de gerenciamento de foco, como os eventos ALT + TAB e Click do mouse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Especifica que o Direct3D não oferece suporte a chamadas get * para qualquer coisa que possa ser armazenada em blocos de estado. Ele também informa ao Direct3D para não fornecer nenhum serviço de emulação para processamento de vértice. Isso significa que, se o dispositivo não oferecer suporte ao processamento de vértice, o aplicativo poderá usar apenas vértices após a transformação.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Permite protetores de tela durante um aplicativo de tela inteira. Sem esse sinalizador, o Direct3D desabilitará os protetores de tela, desde que o aplicativo de chamada esteja em tela inteira. Se o aplicativo de chamada já for um protetor de tela, esse sinalizador não terá efeito. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING e D3DCREATE \_ software \_ VERTEXPROCESSING são sinalizadores mutuamente exclusivos. Pelo menos um desses sinalizadores de processamento de vértice deve ser especificado ao chamar [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).

## <a name="constant-information"></a>Informações constantes



| Requisito                         |  Valor          |
|--------------------------|------------|
| parâmetro                   | D3D9. h     |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
