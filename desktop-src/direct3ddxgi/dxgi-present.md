---
description: As constantes do DXGI \_ presente especificam opções para apresentar quadros à saída.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797621"
---
# <a name="dxgi_present"></a>DXGI \_ presente

As constantes do **dxgi \_ presente** especificam opções para apresentar quadros à saída.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">Apresente um quadro de cada buffer (começando com o buffer atual) para a saída.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Apresente um quadro do buffer atual para a saída. Use esse sinalizador para que a apresentação possa usar a sincronização vertical em branco em vez de sequenciar os buffers na cadeia da maneira usual.<br/>
<blockquote>
[!Note]<br />
Se o aplicativo de chamada definir a constante DXGI_PRESENT_DO_NOT_SEQUENCE na primeira operação presente (ou seja, quando não houver um buffer atual), o tempo de execução ignorará essa operação e não chamará o driver.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Não apresente o quadro à saída. O status da cadeia de permuta será testado e os erros apropriados serão retornados. DXGI_PRESENT_TEST destina-se ao uso somente ao alternar do estado ocioso; Não use-o para determinar quando alternar para o estado ocioso porque fazer isso pode deixar a cadeia de permuta incapaz de sair do modo de tela inteira.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Especifica que o tempo de execução descartará os presentes na fila pendentes.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Especifica que o tempo de execução falhará na apresentação (ou seja, falhará em uma chamada para <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) com o código de erro <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> se o thread de chamada estiver bloqueado; o tempo de execução retorna DXGI_ERROR_WAS_STILL_DRAWING em vez de entrar em suspensão até que a dependência seja resolvida.<br/> <strong>Direct3D 11:</strong> Esse valor de enumeração tem suporte a partir do Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Indica que o conteúdo da apresentação será mostrado apenas na saída específica. O conteúdo não será visível em outras saídas. Por exemplo, se o usuário tentar realocar o conteúdo de vídeo em outra saída, o conteúdo de vídeo não ficará visível. <br/> <strong>Direct3D 11:</strong> Esse valor de enumeração tem suporte a partir do Windows 8. <br/>
<blockquote>
[!Note]<br />
Esse sinalizador só deve ser usado com o efeito de permuta <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> ou DXGI_SWAP_EFFECT_FLIP_DISCARD. O uso desse sinalizador com <em>outros</em> efeitos de permuta está sendo preterido e pode não funcionar em versões futuras do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Indica que, se o estéreo presente precisar ser reduzido para mono, a exibição do olho direito será usada em vez da exibição de olho à esquerda.<br/> <strong>Direct3D 11:</strong> Esse valor de enumeração tem suporte a partir do Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Indica que a apresentação deve usar o buffer esquerdo como um buffer mono. Um aplicativo chama o método <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1:: IsTemporaryMonoSupported</strong></a> para determinar se uma cadeia de permuta dá suporte a &quot; mono temporário &quot; .<br/> <strong>Direct3D 11:</strong> Esse valor de enumeração tem suporte a partir do Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Esse sinalizador deve ser definido por aplicativos de mídia que estão usando uma duração de apresentação personalizada no momento (taxa de atualização personalizada). Consulte <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Esse valor tem suporte a partir de Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Permitir a divisão é um requisito de exibições de taxa de atualização variável.<br/> As condições para usar DXGI_PRESENT_ALLOW_TEARING durante o presente são as seguintes:<br/>
<ul>
<li>A cadeia de permuta deve ser criada com o sinalizador <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> .</li>
<li>O intervalo de sincronização passado para <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>presente</strong></a> (ou <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) deve ser 0.</li>
<li>O sinalizador DXGI_PRESENT_ALLOW_TEARING não pode ser usado em um aplicativo que está atualmente em modo de tela inteira (definido chamando <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>Setfullscreenstate (true)</strong></a>). Ele só pode ser usado no modo de janela. Para usar esse sinalizador em aplicativos de tela inteira do Win32, o aplicativo deve apresentar uma janela sem borda à tela inteira e desabilitar ALT automático + entrar na tela inteira usando <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory:: MakeWindowAssociation</strong></a>. Os aplicativos UWP que entram no modo de tela inteira chamando <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> são janelas sem borda em tela inteira e podem usar o sinalizador.</li>
</ul>
Chamar <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (ou <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) com esse sinalizador e não atender às condições acima resultará em um erro DXGI_ERROR_INVALID_CALL sendo retornado ao aplicativo de chamada.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

As opções de apresentação são fornecidas durante a chamada [**IDXGISwapChain::P reenviada**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) ou [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Os buffers são especificados na descrição [**da cadeia de \_ \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)permuta (consulte a cadeia de permuta de [**dxgi \_ \_ \_**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) de

O DXGI \_ presente \_ reinício é válido somente para cadeias de permuta de flip-Model e tela inteira. Os aplicativos podem usar \_ dxgi \_ que apresentam reinicialização para se recuperar de falhas na reprodução, bem como para descartar apresentações em fila anteriormente. A descartação de apresentações enfileiradas anteriormente será útil se as apresentações em fila forem cenários em janelas. Em particular, a apresentação anteriormente enfileirada pode ter assumido que a janela tem um tamanho antigo (ou seja, uma operação de redimensionamento ocorreu após o envio).

O DXGI \_ presente \_ restrito \_ à \_ saída é válido somente para cadeias de permuta que especificaram uma saída específica para restringir o conteúdo quando essas cadeias de permuta foram criadas ([**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Se não houver nenhuma saída para restringir, o sinalizador será inválido.

DXGI \_ com \_ estéreo \_ \_ de saída de poliverdade indica que, se o estéreo presente precisar ser reduzido para mono, o olho correto deve ser usado em vez do olho esquerdo (padrão). Você pode usar esse sinalizador se um lado for maior qualidade (por exemplo, se o par estéreo for resumido a partir de uma imagem padrão).

DXGI \_ \_ que apresenta estéreo \_ temporário \_ mono indica que a presente deve usar o buffer esquerdo como um buffer mono. Você pode usar esse sinalizador para evitar a atualização do buffer correto quando um aplicativo não tem conteúdo estéreo temporariamente. Você deve usar esse sinalizador sempre que possível, pois ele permite uma otimização significativa pelo sistema operacional e, em algumas circunstâncias, ele pode evitar artefatos de alteração no modo visível.

Você deve usar o \_ \_ \_ sinalizador mono temporário estéreo de dxgi \_ em preferência para alternar para uma cadeia de permuta mono para a maioria dos aplicativos que você prevê que usarão o estéreo novamente. Você precisa equilibrar o uso desse sinalizador em aplicativos que são extremamente executados ou que raramente exibem o estéreo em relação à desvantagem da memória não utilizada.

> [!Note]  
> Aplicativos de tela inteira que alternam para uma cadeia de permuta mono causam uma alteração de modo que geralmente tem artefatos visíveis (por exemplo, "piscando"). No entanto, o mono temporário pode não ter suporte para cadeias de troca de tela inteira.

 

O estéreo de DXGI \_ presente \_ Stereo a \_ \_ direita e dxgi \_ apresentam \_ \_ sinalizadores mono temporários estéreos \_ só se aplicam a cadeias de permuta estéreo. Se você usá-los quando apresentar cadeias de permuta mono, ocorrerá uma operação inválida.

Se você usar o \_ \_ \_ sinalizador mono temporário estéreo de dxgi \_ ao apresentar uma cadeia de permuta estéreo que não dá suporte a mono temporário, ocorrerá um erro, a cadeia de permuta não será exibida e a apresentação retornará uma [chamada de \_ erro dxgi \_ \_ inválida](dxgi-error.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
