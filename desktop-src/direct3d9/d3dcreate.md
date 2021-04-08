---
description: Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920468"
---
# <a name="d3dcreate"></a><span data-ttu-id="16f58-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="16f58-103">D3DCREATE</span></span>

<span data-ttu-id="16f58-104">Uma combinação de um ou mais sinalizadores que controlam o comportamento de criação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16f58-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16f58-105">#definir</span><span class="sxs-lookup"><span data-stu-id="16f58-105">#define</span></span></td>
<td><span data-ttu-id="16f58-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="16f58-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="16f58-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="16f58-108">O aplicativo solicita que o dispositivo conduza todos os cabeçotes que esse adaptador mestre possui.</span><span class="sxs-lookup"><span data-stu-id="16f58-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="16f58-109">O sinalizador é inválido em adaptadores não mestres.</span><span class="sxs-lookup"><span data-stu-id="16f58-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="16f58-110">Se esse sinalizador for definido, os parâmetros de apresentação passados para <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> deverão apontar para uma matriz de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="16f58-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="16f58-111">O número de elementos em <strong>D3DPRESENT_PARAMETERS</strong> deve ser igual ao número de adaptadores definidos pelo membro NumberOfAdaptersInGroup da estrutura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="16f58-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="16f58-112">O tempo de execução do DirectX atribuirá cada elemento a cada cabeçalho na ordem numérica especificada pelo membro AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</span><span class="sxs-lookup"><span data-stu-id="16f58-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="16f58-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="16f58-114">O Direct3D gerenciará recursos em vez do driver.</span><span class="sxs-lookup"><span data-stu-id="16f58-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="16f58-115">As chamadas Direct3D não falharão para erros de recurso, como memória de vídeo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="16f58-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="16f58-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="16f58-117">Como D3DCREATE_DISABLE_DRIVER_MANAGEMENT, o Direct3D gerenciará os recursos em vez do driver.</span><span class="sxs-lookup"><span data-stu-id="16f58-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="16f58-118">Ao contrário de D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX retornará erros para condições como memória de vídeo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="16f58-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="16f58-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="16f58-120">Faz com que o tempo de execução não Registre as teclas de captura para a tela, Ctrl-Printscreen e Alt-Printscreen para capturar o conteúdo da área de trabalho ou da janela.</span><span class="sxs-lookup"><span data-stu-id="16f58-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16f58-121">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="16f58-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="16f58-122">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="16f58-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="16f58-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="16f58-124">Restrinja a computação ao thread do aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="16f58-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="16f58-125">Se o sinalizador não estiver definido, o tempo de execução poderá executar o processamento de vértice de software e outros cálculos no thread de trabalho para melhorar o desempenho em sistemas com vários processadores.</span><span class="sxs-lookup"><span data-stu-id="16f58-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16f58-126">Diferenças entre o Windows XP e o Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="16f58-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="16f58-127">Esse sinalizador está disponível no Windows Vista, no Windows Server 2008 e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16f58-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="16f58-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="16f58-129">Habilita a coleta de estatísticas atuais no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16f58-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="16f58-130">Chamadas para <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> retornarão dados válidos.</span><span class="sxs-lookup"><span data-stu-id="16f58-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16f58-131">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="16f58-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="16f58-132">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="16f58-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="16f58-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="16f58-134">Defina a precisão para cálculos de ponto flutuante do Direct3D para a precisão usada pelo thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="16f58-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="16f58-135">Se você não especificar esse sinalizador, o Direct3D usa como padrão o modo de ida e volta de precisão simples por dois motivos:</span><span class="sxs-lookup"><span data-stu-id="16f58-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="16f58-136">O modo de precisão dupla reduzirá o desempenho do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="16f58-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="16f58-137">Partes do Direct3D pressupõem que as exceções de unidade de ponto flutuante são mascaradas; a remoção de máscara dessas exceções pode resultar em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="16f58-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="16f58-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="16f58-139">Especifica o processamento de vértice de hardware.</span><span class="sxs-lookup"><span data-stu-id="16f58-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="16f58-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="16f58-141">Especifica o processamento de vértice misto (software e hardware).</span><span class="sxs-lookup"><span data-stu-id="16f58-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="16f58-142">Para o Windows 10, versão 1607 e posterior, não é recomendável usar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="16f58-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="16f58-143">Consulte D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="16f58-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="16f58-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="16f58-145">Especifica o processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="16f58-145">Specifies software vertex processing.</span></span> <span data-ttu-id="16f58-146">Para o Windows 10, versão 1607 e posterior, não é recomendável usar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="16f58-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="16f58-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="16f58-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="16f58-148">A menos que o processamento de vértice de hardware não esteja disponível, o uso do processamento de vértice de software não é recomendado no Windows 10, versão 1607 (e versões posteriores) porque a eficiência do processamento de vértice de software foi significativamente reduzida e, ao mesmo tempo, melhora a segurança da implementação.</span><span class="sxs-lookup"><span data-stu-id="16f58-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="16f58-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="16f58-150">Indica que o aplicativo solicita que o Direct3D seja multithread seguro.</span><span class="sxs-lookup"><span data-stu-id="16f58-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="16f58-151">Isso faz com que um thread Direct3D assuma a propriedade de sua <a href="/windows/desktop/Sync/critical-section-objects">seção crítica</a> global com mais frequência, o que pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="16f58-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="16f58-152">Se um aplicativo processar mensagens de janela em um thread ao fazer chamadas de API do Direct3D em outro, o aplicativo deverá usar esse sinalizador ao criar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16f58-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="16f58-153">Essa janela também deve ser destruída antes de descarregar d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="16f58-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="16f58-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="16f58-155">Indica que o Direct3D não deve alterar a janela de foco de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="16f58-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="16f58-156">Se esse sinalizador for definido, o aplicativo deverá oferecer suporte total a todos os eventos de gerenciamento de foco, como os eventos ALT + TAB e Click do mouse.</span><span class="sxs-lookup"><span data-stu-id="16f58-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16f58-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="16f58-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="16f58-158">Especifica que o Direct3D não oferece suporte a chamadas get \* para qualquer coisa que possa ser armazenada em blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="16f58-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="16f58-159">Ele também informa ao Direct3D para não fornecer nenhum serviço de emulação para processamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="16f58-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="16f58-160">Isso significa que, se o dispositivo não oferecer suporte ao processamento de vértice, o aplicativo poderá usar apenas vértices após a transformação.</span><span class="sxs-lookup"><span data-stu-id="16f58-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16f58-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="16f58-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="16f58-162">Permite protetores de tela durante um aplicativo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="16f58-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="16f58-163">Sem esse sinalizador, o Direct3D desabilitará os protetores de tela, desde que o aplicativo de chamada esteja em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="16f58-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="16f58-164">Se o aplicativo de chamada já for um protetor de tela, esse sinalizador não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="16f58-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16f58-165">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="16f58-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="16f58-166">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="16f58-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="16f58-167">D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING e D3DCREATE \_ software \_ VERTEXPROCESSING são sinalizadores mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="16f58-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="16f58-168">Pelo menos um desses sinalizadores de processamento de vértice deve ser especificado ao chamar [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="16f58-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="16f58-169">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="16f58-169">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="16f58-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16f58-170">Header</span></span>                   | <span data-ttu-id="16f58-171">D3D9. h</span><span class="sxs-lookup"><span data-stu-id="16f58-171">D3D9.h</span></span>     |
| <span data-ttu-id="16f58-172">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="16f58-172">Minimum operating system</span></span> | <span data-ttu-id="16f58-173">Windows 98</span><span class="sxs-lookup"><span data-stu-id="16f58-173">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="16f58-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16f58-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f58-175">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="16f58-175">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
