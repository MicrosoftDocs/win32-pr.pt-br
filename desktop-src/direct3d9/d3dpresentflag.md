---
description: Constantes usadas por \_ parâmetros D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760535"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="a86e3-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="a86e3-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="a86e3-104">Constantes usadas por [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a86e3-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-105">#definir</span><span class="sxs-lookup"><span data-stu-id="a86e3-105">#define</span></span></td>
<td><span data-ttu-id="a86e3-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a86e3-106">Value</span></span></td>
<td><span data-ttu-id="a86e3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a86e3-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="a86e3-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="a86e3-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a86e3-109">0x00000004</span></span></td>
<td><span data-ttu-id="a86e3-110">Cortar um blit <a href="/windows/desktop/api"><strong>presente</strong></a> em janelas na área do cliente do Windows, na área da tela monitor do adaptador de vídeo que criou o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a86e3-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="a86e3-111">D3DPRESENTFLAG_DEVICECLIP não é válido com D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="a86e3-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a86e3-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="a86e3-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="a86e3-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a86e3-113">0x00000002</span></span></td>
<td><span data-ttu-id="a86e3-114">Defina esse sinalizador quando o dispositivo ou a cadeia de troca for criada para habilitar a descartação do buffer z.</span><span class="sxs-lookup"><span data-stu-id="a86e3-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="a86e3-115">Se esse sinalizador for definido, o conteúdo do buffer do estêncil de profundidade será inválido após a chamada de <a href="/windows/desktop/api"><strong>presente</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> com uma superfície de profundidade diferente.</span><span class="sxs-lookup"><span data-stu-id="a86e3-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="a86e3-116">Descartar os dados do buffer z pode aumentar o desempenho e depende do driver.</span><span class="sxs-lookup"><span data-stu-id="a86e3-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="a86e3-117">O tempo de execução de depuração impedirá a descartação desmarcando o z-buffer para algum valor constante depois de chamar <a href="/windows/desktop/api"><strong>Present</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> com uma superfície de profundidade diferente.</span><span class="sxs-lookup"><span data-stu-id="a86e3-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="a86e3-118">Descartar dados do buffer z é ilegal para todos os formatos bloqueáveis, D3DFMT_D16_LOCKABLE e D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="a86e3-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="a86e3-119">Qualquer uso de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> especificando um formato bloqueáveis e a descartação do buffer z falhará.</span><span class="sxs-lookup"><span data-stu-id="a86e3-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="a86e3-120">Para obter mais informações sobre formatos, consulte <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="a86e3-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="a86e3-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="a86e3-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a86e3-122">0x00000001</span></span></td>
<td><span data-ttu-id="a86e3-123">Defina esse sinalizador se o aplicativo exigir a capacidade de bloquear o buffer de fundo diretamente.</span><span class="sxs-lookup"><span data-stu-id="a86e3-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="a86e3-124">Observe que os buffers de fundo não são bloqueáveis, a menos que o aplicativo especifique D3DPRESENTFLAG_LOCKABLE_BACKBUFFER ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> ou <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a86e3-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="a86e3-125">Os buffers de fundo do bloqueáveis incorrem em um custo de desempenho em algumas configurações de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a86e3-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="a86e3-126">Executar uma operação de bloqueio (ou usar <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> para gravar) no buffer de back bloqueáveis diminui o desempenho em muitos cartões.</span><span class="sxs-lookup"><span data-stu-id="a86e3-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="a86e3-127">Nesse caso, considere o uso de triângulos texturizados para mover dados para o buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="a86e3-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-128">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-129">No Direct3D9Ex, esse sinalizador não poderá ser definido se o D3DSWAPEFFECT estiver D3DSWAPEFFECT_FLIPEX, já que o modelo Inverter permite que o Gerenciador de Janelas da Área de Trabalho acesse o buffer de fundo de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a86e3-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="a86e3-130">Uma superfície compartilhada entre processos não deve ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a86e3-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a86e3-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="a86e3-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="a86e3-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a86e3-132">0x00000020</span></span></td>
<td><span data-ttu-id="a86e3-133">Os monitores girados são manipulados automaticamente com uma cópia giratória durante a apresentação, o que não é muito eficiente.</span><span class="sxs-lookup"><span data-stu-id="a86e3-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="a86e3-134">Esse sinalizador significa que o aplicativo executará sua própria rotação de exibição.</span><span class="sxs-lookup"><span data-stu-id="a86e3-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-135">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-136">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="a86e3-137">Os aplicativos podem atingir sua própria rotação possivelmente usando uma matriz de exibição girada.</span><span class="sxs-lookup"><span data-stu-id="a86e3-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="a86e3-138">Os métodos <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> devem ser usados para localizar a configuração de rotação atual.</span><span class="sxs-lookup"><span data-stu-id="a86e3-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="a86e3-139">Os parâmetros de largura e altura do buffer de totais em <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> devem ser usados na orientação paisagem, enquanto a estrutura do modo de exibição em tela inteira deve ser a mesma que a retornada de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (ou seja, Width e Height são trocados quando girado 90 e 270 graus).</span><span class="sxs-lookup"><span data-stu-id="a86e3-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="a86e3-140">Ao usar o bloqueio em destinos de renderização girados, suposições de canto superior esquerdo não são mais verdadeiras, o destino de renderização SURFACE_DESC permanecerá paisagem (como implícito pelos parâmetros de criação) e janela GDI, coordenadas do mouse e, por isso, precisam ser convertidas corretamente quando usadas com o destino de renderização do Direct3D e a cena.</span><span class="sxs-lookup"><span data-stu-id="a86e3-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="a86e3-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="a86e3-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a86e3-142">0x00000040</span></span></td>
<td><span data-ttu-id="a86e3-143">Use esse sinalizador para especificar qualquer modo de exibição bruto enumerado pelo adaptador de vídeo, embora o Direct3D possa ter indicado que o modo é inválido.</span><span class="sxs-lookup"><span data-stu-id="a86e3-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="a86e3-144">O aplicativo deve implementar isso de maneira robusta, caso o modo desejado realmente seja inválido.</span><span class="sxs-lookup"><span data-stu-id="a86e3-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-145">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-146">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a86e3-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="a86e3-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="a86e3-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a86e3-148">0x00000010</span></span></td>
<td><span data-ttu-id="a86e3-149">Essa é uma dica para o driver que os buffers de fundo conterám dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a86e3-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="a86e3-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="a86e3-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a86e3-151">0x00000080</span></span></td>
<td><span data-ttu-id="a86e3-152">Especifica se a sobreposição é RGB do intervalo completo ou RGB de intervalo limitado.</span><span class="sxs-lookup"><span data-stu-id="a86e3-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="a86e3-153">A definição desse sinalizador indica um intervalo limitado de RGB.</span><span class="sxs-lookup"><span data-stu-id="a86e3-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="a86e3-154">Em um intervalo de RGB limitado, o intervalo RGB é compactado de modo que 16:16:16 é preto e 235:235:235 é branco.</span><span class="sxs-lookup"><span data-stu-id="a86e3-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-155">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-156">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a86e3-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="a86e3-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="a86e3-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="a86e3-158">0x00000100</span></span></td>
<td><span data-ttu-id="a86e3-159">Especifica se a sobreposição é BT. 601 ou BT. 709.</span><span class="sxs-lookup"><span data-stu-id="a86e3-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="a86e3-160">A definição desse sinalizador indica BT. 709, para TV de alta definição (HDTV).</span><span class="sxs-lookup"><span data-stu-id="a86e3-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-161">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-162">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="a86e3-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="a86e3-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="a86e3-164">0x00000200</span></span></td>
<td><span data-ttu-id="a86e3-165">Especifica se a sobreposição é convencional YCbCr ou YCbCr estendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="a86e3-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="a86e3-166">A definição desse sinalizador indica YCbCr estendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="a86e3-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-167">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-168">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a86e3-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="a86e3-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="a86e3-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="a86e3-170">0x00000400</span></span></td>
<td><span data-ttu-id="a86e3-171">Definir esse sinalizador indica que o SwapChain contém conteúdo protegido e automaticamente faz com que o tempo de execução restrinja o acesso ao SwapChain para que apenas o DWM (desktop Windows Manager) possa usar o SwapChain.</span><span class="sxs-lookup"><span data-stu-id="a86e3-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-172">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-173">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a86e3-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="a86e3-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="a86e3-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="a86e3-175">0x00000800</span></span></td>
<td><span data-ttu-id="a86e3-176">A definição desse sinalizador indica que o driver deve restringir o acesso a todos os recursos compartilhados que são criados para interação com o DWM.</span><span class="sxs-lookup"><span data-stu-id="a86e3-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="a86e3-177">O chamador deve criar um canal autenticado com o driver.</span><span class="sxs-lookup"><span data-stu-id="a86e3-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="a86e3-178">O driver deve, então, permitir o acesso a processos que tentam abrir esses recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="a86e3-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a86e3-179">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a86e3-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a86e3-180">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a86e3-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a86e3-181">Essas constantes são usadas por [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a86e3-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a86e3-182">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="a86e3-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="a86e3-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a86e3-183">Header</span></span>                   | <span data-ttu-id="a86e3-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="a86e3-184">d3d9types.h</span></span> |
| <span data-ttu-id="a86e3-185">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="a86e3-185">Minimum operating system</span></span> | <span data-ttu-id="a86e3-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a86e3-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a86e3-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a86e3-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a86e3-188">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a86e3-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




