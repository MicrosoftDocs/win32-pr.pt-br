---
title: Aprimoramentos do Direct3D 9Ex
description: Este tópico descreve o suporte adicionado ao Windows 7 para o modo invertido presente e suas estatísticas atuais associadas no Direct3D 9Ex e no Gerenciador de Janelas da Área de Trabalho.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366471"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="53ecd-103">Aprimoramentos do Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="53ecd-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="53ecd-104">Este tópico descreve o suporte adicionado ao Windows 7 para o modo invertido presente e suas estatísticas atuais associadas no Direct3D 9Ex e no Gerenciador de Janelas da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="53ecd-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="53ecd-105">Os aplicativos de destino incluem aplicativos de apresentação baseados em taxas de vídeo ou quadros.</span><span class="sxs-lookup"><span data-stu-id="53ecd-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="53ecd-106">Os aplicativos que usam o modo de flip do Direct3D 9Ex presente reduzem a carga de recursos do sistema quando o DWM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="53ecd-107">As melhorias de estatísticas atuais associadas ao modo Inverter apresentam a habilitação dos aplicativos do Direct3D 9Ex para controlar melhor a taxa de apresentação, fornecendo comentários em tempo real e mecanismos de correção.</span><span class="sxs-lookup"><span data-stu-id="53ecd-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="53ecd-108">São incluídas explicações e ponteiros detalhados para recursos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="53ecd-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="53ecd-109">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="53ecd-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="53ecd-110">O que melhorou sobre o Direct3D 9Ex para Windows 7</span><span class="sxs-lookup"><span data-stu-id="53ecd-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="53ecd-111">Apresentação do modo de flip do Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="53ecd-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="53ecd-112">Modelo de programação e APIs</span><span class="sxs-lookup"><span data-stu-id="53ecd-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="53ecd-113">Como optar pelo modelo de inversão do Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="53ecd-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="53ecd-114">Diretrizes de design para aplicativos de modelo do Direct3D 9Ex flip</span><span class="sxs-lookup"><span data-stu-id="53ecd-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="53ecd-115">Sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip</span><span class="sxs-lookup"><span data-stu-id="53ecd-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="53ecd-116">Sincronização de quadros para aplicativos em janelas quando o DWM está desativado</span><span class="sxs-lookup"><span data-stu-id="53ecd-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="53ecd-117">Passo a passo de um modelo do Direct3D 9Ex flip e apresentar estatísticas de exemplo</span><span class="sxs-lookup"><span data-stu-id="53ecd-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="53ecd-118">Resumo das recomendações de programação para sincronização de quadros</span><span class="sxs-lookup"><span data-stu-id="53ecd-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="53ecd-119">Conclusão sobre os aprimoramentos do Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="53ecd-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="53ecd-120">Plano de ação</span><span class="sxs-lookup"><span data-stu-id="53ecd-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="53ecd-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53ecd-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="53ecd-122">O que melhorou sobre o Direct3D 9Ex para Windows 7</span><span class="sxs-lookup"><span data-stu-id="53ecd-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="53ecd-123">A apresentação do modo Inverter do Direct3D 9Ex é um modo aprimorado de apresentação de imagens no Direct3D 9Ex que efetivamente transfere imagens renderizadas para o Windows 7 Gerenciador de Janelas da Área de Trabalho (DWM) para composição.</span><span class="sxs-lookup"><span data-stu-id="53ecd-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="53ecd-124">A partir do Windows Vista, o DWM compõe toda a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="53ecd-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="53ecd-125">Quando o DWM está habilitado, os aplicativos de modo em janela apresentam seu conteúdo na área de trabalho usando um método chamado modo blt presente para DWM (ou modelo BLT).</span><span class="sxs-lookup"><span data-stu-id="53ecd-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="53ecd-126">Com o modelo BLT, o DWM mantém uma cópia da superfície do Direct3D 9Ex renderizada para composição de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="53ecd-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="53ecd-127">Quando o aplicativo é atualizado, o novo conteúdo é copiado para a superfície do DWM por meio de um blt.</span><span class="sxs-lookup"><span data-stu-id="53ecd-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="53ecd-128">Para aplicativos que contêm conteúdo de Direct3D e GDI, os dados GDI também são copiados na superfície do DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="53ecd-129">Disponível no Windows 7, o modo flip presente para DWM (ou flip Model) é um novo método de apresentação que essencialmente habilita a passagem de identificadores de superfícies de aplicativos entre aplicativos de modo em janelas e DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="53ecd-130">Além de salvar recursos, o flip Model dá suporte a estatísticas de apresentação avançadas.</span><span class="sxs-lookup"><span data-stu-id="53ecd-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="53ecd-131">As estatísticas atuais são informações de tempo de quadro que os aplicativos podem usar para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="53ecd-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="53ecd-132">As informações de tempo de quadro em estatísticas atuais permitem que os aplicativos ajustem a taxa de apresentação de seus quadros de vídeo para uma apresentação mais suave.</span><span class="sxs-lookup"><span data-stu-id="53ecd-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="53ecd-133">No Windows Vista, em que o DWM mantém uma cópia correspondente da superfície do quadro para composição de área de trabalho, os aplicativos podem usar as estatísticas atuais fornecidas pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="53ecd-134">Esse método de obtenção de estatísticas presentes ainda estará disponível no Windows 7 para aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="53ecd-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="53ecd-135">No Windows 7, os aplicativos baseados no Direct3D 9Ex que adotam o flip Model devem usar APIs D3D9Ex para obter estatísticas atuais.</span><span class="sxs-lookup"><span data-stu-id="53ecd-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="53ecd-136">Quando o DWM está habilitado, o modo em janela e o modo exclusivo de tela inteira aplicativos do Direct3D 9Ex podem esperar as mesmas informações de estatísticas presentes ao usar o flip Model.</span><span class="sxs-lookup"><span data-stu-id="53ecd-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="53ecd-137">As estatísticas do Direct3D 9Ex flip Model presente permitem que os aplicativos consultem as estatísticas atuais em tempo real, em vez de após o quadro ter sido mostrado na tela; as mesmas informações de estatísticas presentes estão disponíveis para aplicativos habilitados para o modo de Flip-Model de janela como aplicativos de tela inteira; um sinalizador adicionado nas APIs D3D9Ex permite que os aplicativos de modelo de inversão descartem com eficiência quadros atrasados no momento da apresentação.</span><span class="sxs-lookup"><span data-stu-id="53ecd-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="53ecd-138">O modelo de flip do Direct3D 9Ex deve ser usado por novos aplicativos de apresentação baseados em taxas de vídeo ou quadros direcionados ao Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53ecd-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="53ecd-139">Devido à sincronização entre o DWM e o tempo de execução do Direct3D 9Ex, os aplicativos que usam o modelo de flip devem especificar entre 2 e 4 buffers de reversão para garantir uma apresentação suave.</span><span class="sxs-lookup"><span data-stu-id="53ecd-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="53ecd-140">Esses aplicativos que usam informações de estatísticas atuais se beneficiarão do uso dos aprimoramentos de estatísticas presentes do flip Model habilitado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="53ecd-141">Apresentação do modo de flip do Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="53ecd-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="53ecd-142">As melhorias de desempenho do modo de inversão do Direct3D 9Ex presentes são significativas no sistema quando o DWM está ativado e quando o aplicativo está no modo de janela, em vez de em modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="53ecd-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="53ecd-143">A tabela e a ilustração a seguir mostram uma comparação simplificada de usos de largura de banda de memória e leituras do sistema e gravações de aplicativos em janelas que escolhem o modelo de flip versus o modelo de BLT de uso padrão.</span><span class="sxs-lookup"><span data-stu-id="53ecd-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="53ecd-144">Modo blt presente para DWM</span><span class="sxs-lookup"><span data-stu-id="53ecd-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="53ecd-145">Modo flip D3D9Ex presente para DWM</span><span class="sxs-lookup"><span data-stu-id="53ecd-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="53ecd-146">1. o aplicativo atualiza seu quadro (gravação)</span><span class="sxs-lookup"><span data-stu-id="53ecd-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="53ecd-147">1. o aplicativo atualiza seu quadro (gravação)</span><span class="sxs-lookup"><span data-stu-id="53ecd-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="53ecd-148">2. o tempo de execução do Direct3D copia o conteúdo da superfície para uma superfície de redirecionamento do DWM (leitura, gravação)</span><span class="sxs-lookup"><span data-stu-id="53ecd-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="53ecd-149">2. o tempo de execução do Direct3D passa a superfície do aplicativo para o DWM</span><span class="sxs-lookup"><span data-stu-id="53ecd-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="53ecd-150">3. após a cópia da superfície compartilhada ser concluída, o DWM renderiza a superfície do aplicativo na tela (leitura, gravação)</span><span class="sxs-lookup"><span data-stu-id="53ecd-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="53ecd-151">3. o DWM renderiza a superfície do aplicativo na tela (leitura, gravação)</span><span class="sxs-lookup"><span data-stu-id="53ecd-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![ilustração de uma comparação do modelo BLT e do flip Model](images/blt-flip-mode-present.png)

<span data-ttu-id="53ecd-153">O modo Inverter apresenta redução do uso de memória do sistema, reduzindo o número de leituras e gravações pelo tempo de execução do Direct3D para a composição de quadro em janela pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="53ecd-154">Isso reduz o consumo de energia do sistema e o uso geral da memória.</span><span class="sxs-lookup"><span data-stu-id="53ecd-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="53ecd-155">Os aplicativos podem tirar proveito do modo Inverter do Direct3D 9Ex presente nas melhorias de estatísticas quando o DWM está ativado, independentemente de o aplicativo estar no modo de janela ou em modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="53ecd-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="53ecd-156">Modelo de programação e APIs</span><span class="sxs-lookup"><span data-stu-id="53ecd-156">Programming Model and APIs</span></span>

<span data-ttu-id="53ecd-157">Nova taxa de vídeo ou quadro-os aplicativos medir que usam as APIs do Direct3D 9Ex no Windows 7 podem tirar proveito da memória e da economia de energia e da apresentação aprimorada oferecida pelo modo invertido presente durante a execução no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53ecd-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="53ecd-158">(Ao executar em versões anteriores do Windows, o tempo de execução do Direct3D usa como padrão o aplicativo para o modo blt presente.)</span><span class="sxs-lookup"><span data-stu-id="53ecd-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="53ecd-159">O modo Inverter significa que o aplicativo pode aproveitar os comentários de estatísticas e os mecanismos de correção presentes em tempo real quando o DWM está ativado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="53ecd-160">No entanto, os aplicativos que usam o modo flip presente devem estar cientes das limitações quando usam a renderização simultânea da API GDI.</span><span class="sxs-lookup"><span data-stu-id="53ecd-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="53ecd-161">Você pode modificar os aplicativos existentes para aproveitar o modo invertido presente, com os mesmos benefícios e limitações que os aplicativos desenvolvidos recentemente.</span><span class="sxs-lookup"><span data-stu-id="53ecd-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="53ecd-162">Como optar pelo modelo de inversão do Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="53ecd-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="53ecd-163">Os aplicativos do Direct3D 9Ex destinados ao Windows 7 podem optar pelo flip Model criando a cadeia de permuta com o valor de enumeração [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="53ecd-164">Para aceitar o modelo de inversão, os aplicativos especificam a estrutura de [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e passam um ponteiro para essa estrutura quando chamam a API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="53ecd-165">Esta seção descreve como os aplicativos destinados ao Windows 7 usam **IDirect3D9Ex:: CreateDeviceEx** para aceitar o modelo de inversão.</span><span class="sxs-lookup"><span data-stu-id="53ecd-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="53ecd-166">Para obter mais informações sobre a API **IDirect3D9Ex:: CreateDeviceEx** , consulte **IDirect3D9Ex:: CreateDeviceEx no MSDN**.</span><span class="sxs-lookup"><span data-stu-id="53ecd-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="53ecd-167">Para sua conveniência, a sintaxe [**dos \_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.</span><span class="sxs-lookup"><span data-stu-id="53ecd-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="53ecd-168">Ao modificar aplicativos do Direct3D 9Ex para o Windows 7 para optar pelo flip Model, você deve considerar os seguintes itens sobre os membros especificados dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):</span><span class="sxs-lookup"><span data-stu-id="53ecd-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="53ecd-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="53ecd-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="53ecd-170">(Somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="53ecd-170">(Windows 7 Only)</span></span>

<span data-ttu-id="53ecd-171">Quando **SwapEffect** é definido como o novo \_ tipo de efeito de cadeia de permuta D3DSWAPEFFECT FLIPEX, a contagem de buffers de fundo deve ser igual ou maior que 2, para evitar uma penalidade de desempenho de aplicativo como resultado da espera do buffer presente anterior a ser liberado pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="53ecd-172">Quando o aplicativo também usa as estatísticas atuais associadas ao D3DSWAPEFFECT \_ FLIPEX, recomendamos que você defina a contagem de buffers de fundo como de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="53ecd-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="53ecd-173">Usar D3DSWAPEFFECT \_ FLIPEX no Windows Vista ou versões anteriores do sistema operacional retornará falha de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="53ecd-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="53ecd-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="53ecd-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="53ecd-175">(Somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="53ecd-175">(Windows 7 Only)</span></span>

<span data-ttu-id="53ecd-176">O novo \_ tipo de efeito de cadeia de permuta D3DSWAPEFFECT FLIPEX designa quando um aplicativo está adotando o modo invertido presente no DWM.</span><span class="sxs-lookup"><span data-stu-id="53ecd-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="53ecd-177">Ele permite que o aplicativo tenha uso mais eficiente de memória e energia, além de permitir que o aplicativo aproveite as estatísticas de tela inteira em modo de janela.</span><span class="sxs-lookup"><span data-stu-id="53ecd-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="53ecd-178">O comportamento do aplicativo de tela inteira não é afetado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="53ecd-179">Se a janela estiver definida como **true** e **SwapEffect** estiver definida como D3DSWAPEFFECT \_ FLIPEX, o tempo de execução criará um buffer de fundo extra e girará qualquer identificador que pertença ao buffer que se torna o buffer frontal no momento da apresentação.</span><span class="sxs-lookup"><span data-stu-id="53ecd-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="53ecd-180">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="53ecd-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="53ecd-181">(Somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="53ecd-181">(Windows 7 Only)</span></span>

<span data-ttu-id="53ecd-182">O sinalizador de [ \_ \_ BackBuffer D3DPRESENTFLAG bloqueáveis](/windows/desktop/direct3d9/d3dpresentflag) não pode ser definido se **SwapEffect** está definido como o novo tipo de efeito de cadeia de permuta [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="53ecd-183">Diretrizes de design para aplicativos de modelo do Direct3D 9Ex flip</span><span class="sxs-lookup"><span data-stu-id="53ecd-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="53ecd-184">Use as diretrizes nas seções a seguir para projetar seus aplicativos de modelo do Direct3D 9Ex flip.</span><span class="sxs-lookup"><span data-stu-id="53ecd-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="53ecd-185">Usar o modo flip presente em um HWND separado do modo blt presente</span><span class="sxs-lookup"><span data-stu-id="53ecd-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="53ecd-186">Os aplicativos devem usar o modo de flip do Direct3D 9Ex presente em um HWND que não é também direcionado por outras APIs, incluindo o modo blt presente Direct3D 9Ex, outras versões do Direct3D ou GDI.</span><span class="sxs-lookup"><span data-stu-id="53ecd-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="53ecd-187">O modo invertido presente pode ser usado para apresentar janelas filhas; ou seja, os aplicativos podem usar o flip Model quando não são misturados com o modelo BLT no mesmo HWND, conforme mostrado nas ilustrações a seguir.</span><span class="sxs-lookup"><span data-stu-id="53ecd-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![ilustração da janela pai do Direct3D e uma janela filho GDI, cada uma com seu próprio HWND](images/parent-d3d.png)

![ilustração da janela pai do GDI e uma janela filho do Direct3D, cada uma com seu próprio HWND](images/parent-gdi.png)

<span data-ttu-id="53ecd-190">Como o modelo BLT mantém uma cópia adicional da superfície, o GDI e outros conteúdos do Direct3D podem ser adicionados ao mesmo HWND por meio de atualizações por etapas do Direct3D e GDI.</span><span class="sxs-lookup"><span data-stu-id="53ecd-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="53ecd-191">Usando o modelo inverter, somente o conteúdo do Direct3D 9Ex nas cadeias de permuta do [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) que são transmitidas para o DWM será visível.</span><span class="sxs-lookup"><span data-stu-id="53ecd-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="53ecd-192">Todas as outras atualizações de conteúdo do modelo BLT Direct3D ou GDI serão ignoradas, conforme mostrado nas ilustrações a seguir.</span><span class="sxs-lookup"><span data-stu-id="53ecd-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![ilustração de texto GDI que pode não ser exibido se o modelo de flip for usado e o conteúdo do Direct3D e GDI estiverem no mesmo HWND](images/d3d-gdi-same-hwnd.png)

![ilustração do conteúdo de Direct3D e GDI no qual o DWM está habilitado e o aplicativo está no modo de janela](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="53ecd-195">Portanto, o modelo de inversão deve ser habilitado para superfícies de buffers de cadeia de permuta em que o modelo do Direct3D 9Ex flip sozinho é renderizado para o HWND inteiro.</span><span class="sxs-lookup"><span data-stu-id="53ecd-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="53ecd-196">Não use o modelo de flip com ScrollWindow ou ScrollWindowEx da GDI</span><span class="sxs-lookup"><span data-stu-id="53ecd-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="53ecd-197">Alguns aplicativos do Direct3D 9Ex usam as funções ScrollWindow ou ScrollWindowEx da GDI para atualizar o conteúdo da janela quando um evento Scroll do usuário é disparado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="53ecd-198">ScrollWindow e ScrollWindowEx executam BLTS do conteúdo da janela na tela, uma vez que uma janela é rolada.</span><span class="sxs-lookup"><span data-stu-id="53ecd-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="53ecd-199">Essas funções também exigem atualizações de modelo BLT para conteúdo GDI e Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="53ecd-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="53ecd-200">Os aplicativos que usam qualquer função não exibirão, necessariamente, a rolagem do conteúdo da janela visível na tela quando o aplicativo estiver no modo de janela e o DWM estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="53ecd-201">Recomendamos que você não use as APIs ScrollWindow e ScrollWindowEx da GDI em seus aplicativos e, em vez disso, redesenhe seu conteúdo na tela em resposta à rolagem.</span><span class="sxs-lookup"><span data-stu-id="53ecd-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="53ecd-202">Usar uma \_ cadeia de permuta D3DSWAPEFFECT FLIPEX por HWND</span><span class="sxs-lookup"><span data-stu-id="53ecd-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="53ecd-203">Os aplicativos que usam o modelo de flip não devem usar várias cadeias de permuta de modelo invertidas direcionando o mesmo HWND.</span><span class="sxs-lookup"><span data-stu-id="53ecd-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="53ecd-204">Sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip</span><span class="sxs-lookup"><span data-stu-id="53ecd-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="53ecd-205">As estatísticas atuais são informações de temporização de quadro que os aplicativos de mídia usam para sincronizar fluxos de áudio e vídeo e recuperar-se de problemas de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="53ecd-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="53ecd-206">Para habilitar a disponibilidade de estatísticas atuais, o aplicativo Direct3D 9Ex deve garantir que o parâmetro *BehaviorFlags* que o aplicativo passa para [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contém o sinalizador de comportamento do dispositivo [D3DCREATE \_ habilitar \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span><span class="sxs-lookup"><span data-stu-id="53ecd-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="53ecd-207">Para sua conveniência, a sintaxe de [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.</span><span class="sxs-lookup"><span data-stu-id="53ecd-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="53ecd-208">O modelo de flip do Direct3D 9Ex adiciona o sinalizador de apresentação do [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que impõe o comportamento da apresentação [ \_ \_ imediata do intervalo de D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="53ecd-209">O aplicativo Direct3D 9Ex especifica esses sinalizadores de apresentação no parâmetro *dwFlags* que o aplicativo passa para [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="53ecd-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="53ecd-210">Ao modificar seu aplicativo Direct3D 9Ex para o Windows 7, você deve considerar as seguintes informações sobre os sinalizadores de apresentação [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) especificados:</span><span class="sxs-lookup"><span data-stu-id="53ecd-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="53ecd-211">D3DPRESENT \_ DONOTFLIP</span><span class="sxs-lookup"><span data-stu-id="53ecd-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="53ecd-212">Esse sinalizador está disponível somente no modo de tela inteira ou</span><span class="sxs-lookup"><span data-stu-id="53ecd-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="53ecd-213">(Somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="53ecd-213">(Windows 7 Only)</span></span>

<span data-ttu-id="53ecd-214">Quando o aplicativo define o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) para [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="53ecd-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="53ecd-215">D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="53ecd-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="53ecd-216">(Somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="53ecd-216">(Windows 7 Only)</span></span>

<span data-ttu-id="53ecd-217">Esse sinalizador só poderá ser especificado se o aplicativo definir o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) para [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="53ecd-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="53ecd-218">O aplicativo pode usar esse sinalizador para atualizar imediatamente uma superfície com vários quadros posteriormente na fila do DWM presente, essencialmente ignorando os quadros intermediários.</span><span class="sxs-lookup"><span data-stu-id="53ecd-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="53ecd-219">Os aplicativos com janela habilitada para FlipEx podem usar esse sinalizador para atualizar imediatamente uma superfície com um quadro posterior na fila do DWM presente, ignorando os quadros intermediários.</span><span class="sxs-lookup"><span data-stu-id="53ecd-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="53ecd-220">Isso é especialmente útil para aplicativos de mídia que desejam descartar os quadros que foram detectados como atrasados e apresentar quadros subsequentes no momento da composição.</span><span class="sxs-lookup"><span data-stu-id="53ecd-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="53ecd-221">[**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retornará um erro de parâmetro inválido se esse sinalizador estiver incorretamente especificado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="53ecd-222">Para obter informações de estatísticas presentes, o aplicativo obtém a estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chamando a API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="53ecd-223">A estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contém estatísticas sobre [**IDirect3DDevice9Ex::P chamadas resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="53ecd-224">O dispositivo deve ser criado usando uma chamada [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) com o sinalizador [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="53ecd-225">Caso contrário, os dados retornados por [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="53ecd-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="53ecd-226">Uma cadeia de permuta do Direct3D 9Ex habilitada para o flip-Model fornece informações de estatísticas presentes nos modos de tela inteira e em janelas.</span><span class="sxs-lookup"><span data-stu-id="53ecd-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="53ecd-227">Para cadeias de permuta do Direct3D 9Ex habilitadas para modelos BLT no modo de janela, todos os valores de estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serão zerados.</span><span class="sxs-lookup"><span data-stu-id="53ecd-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="53ecd-228">Para as estatísticas presentes do FlipEx, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) retorna D3DERR \_ \_ as estatísticas presentes \_ nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="53ecd-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="53ecd-229">Primeira chamada para [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , que indica o início de uma sequência</span><span class="sxs-lookup"><span data-stu-id="53ecd-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="53ecd-230">Transição do DWM de ativado para desativado</span><span class="sxs-lookup"><span data-stu-id="53ecd-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="53ecd-231">Alteração de modo: qualquer modo de janela para ou de tela inteira ou tela inteira para transições de tela inteira</span><span class="sxs-lookup"><span data-stu-id="53ecd-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="53ecd-232">Para sua conveniência, a sintaxe de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é repetida aqui.</span><span class="sxs-lookup"><span data-stu-id="53ecd-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="53ecd-233">O método [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna o último PresentCount, ou seja, a ID atual da última chamada presente com êxito que foi feita por um dispositivo de vídeo associado à cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="53ecd-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="53ecd-234">Essa ID atual é o valor do membro **PresentCount** da estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) .</span><span class="sxs-lookup"><span data-stu-id="53ecd-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="53ecd-235">Para cadeias de permuta do Direct3D 9Ex habilitadas para modelos BLT, enquanto estiver no modo de janela, todos os valores de estrutura **D3DPRESENTSTATS** serão zerados.</span><span class="sxs-lookup"><span data-stu-id="53ecd-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="53ecd-236">Para sua conveniência, a sintaxe de [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) é repetida aqui.</span><span class="sxs-lookup"><span data-stu-id="53ecd-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="53ecd-237">Ao modificar seu aplicativo Direct3D 9Ex para o Windows 7, você deve considerar as seguintes informações sobre a estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :</span><span class="sxs-lookup"><span data-stu-id="53ecd-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="53ecd-238">O valor de PresentCount que o [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna não é atualizado quando uma chamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT \_ DONOTWAIT especificado no parâmetro *dwFlags* retorna uma falha.</span><span class="sxs-lookup"><span data-stu-id="53ecd-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="53ecd-239">Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) é chamado com D3DPRESENT \_ DONOTFLIP, uma chamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é executada com sucesso, mas não retorna uma estrutura de [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="53ecd-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="53ecd-240">**PresentRefreshCount** versus **SyncRefreshCount** em [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="53ecd-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="53ecd-241">**PresentRefreshCount** é igual a **SyncRefreshCount** quando o aplicativo apresenta em cada vsync.</span><span class="sxs-lookup"><span data-stu-id="53ecd-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="53ecd-242">**SyncRefreshCount** é obtido no intervalo de vsync quando o presente foi enviado, **SyncQPCTime** é aproximadamente o tempo associado ao intervalo de vsync.</span><span class="sxs-lookup"><span data-stu-id="53ecd-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="53ecd-243">Sincronização de quadros para aplicativos em janelas quando o DWM está desativado</span><span class="sxs-lookup"><span data-stu-id="53ecd-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="53ecd-244">Quando o DWM está desativado, os aplicativos em janelas são exibidos diretamente na tela do monitor sem passar por uma cadeia invertida.</span><span class="sxs-lookup"><span data-stu-id="53ecd-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="53ecd-245">No Windows Vista, não há suporte para obter informações de estatísticas de quadro para aplicativos em janelas quando o DWM está desativado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="53ecd-246">Para manter uma API em que os aplicativos não precisam reconhecer o DWM, o Windows 7 retornará informações de estatísticas de quadro para aplicativos em janelas quando o DWM estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="53ecd-247">As estatísticas de quadro retornadas quando o DWM está desativado são apenas estimativas.</span><span class="sxs-lookup"><span data-stu-id="53ecd-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="53ecd-248">Walk-Through de um modelo do Direct3D 9Ex flip e apresentar estatísticas de exemplo</span><span class="sxs-lookup"><span data-stu-id="53ecd-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="53ecd-249">**Para aceitar o exemplo de apresentação do FlipEx para Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="53ecd-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="53ecd-250">Verifique se o aplicativo de exemplo está em execução na versão do sistema operacional Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="53ecd-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="53ecd-251">Defina o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) como [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="53ecd-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="53ecd-252">**Para também optar por FlipEx estatísticas presentes associadas para o exemplo do Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="53ecd-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="53ecd-253">Defina [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) no parâmetro *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="53ecd-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="53ecd-254">**Para evitar, detectar e recuperar-se de falhas**</span><span class="sxs-lookup"><span data-stu-id="53ecd-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="53ecd-255">Enfileirar chamadas presentes: a contagem de BackBuffer recomendada é de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="53ecd-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="53ecd-256">O exemplo do Direct3D 9Ex adiciona um BackBuffer implícito, o comprimento real da fila atual é a contagem de backbuffers + 1.</span><span class="sxs-lookup"><span data-stu-id="53ecd-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="53ecd-257">Criar uma estrutura de fila presente auxiliar para armazenar todas as PresentCount (ID presente) do presente com êxito e associado, calculado/esperado PresentRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="53ecd-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="53ecd-258">Para detectar a ocorrência de falha:</span><span class="sxs-lookup"><span data-stu-id="53ecd-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="53ecd-259">Chame [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="53ecd-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="53ecd-260">Obtenha a ID atual (PresentCount) e a contagem de vsync em que o quadro é mostrado (PresentRefreshCount) do quadro cujas estatísticas atuais são obtidas.</span><span class="sxs-lookup"><span data-stu-id="53ecd-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="53ecd-261">Recupere o PresentRefreshCount esperado (TargetRefresh no código de exemplo) associado à ID atual.</span><span class="sxs-lookup"><span data-stu-id="53ecd-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="53ecd-262">Se o PresentRefreshCount real for posterior ao esperado, ocorrerá uma falha.</span><span class="sxs-lookup"><span data-stu-id="53ecd-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="53ecd-263">Para se recuperar do problema:</span><span class="sxs-lookup"><span data-stu-id="53ecd-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="53ecd-264">Calcule quantos quadros ignorar (a variável g \_ iImmediates no código de exemplo).</span><span class="sxs-lookup"><span data-stu-id="53ecd-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="53ecd-265">Apresente os quadros ignorados com o intervalo D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="53ecd-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="53ecd-266">**Considerações sobre detecção e recuperação de problemas**</span><span class="sxs-lookup"><span data-stu-id="53ecd-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="53ecd-267">A recuperação de problemas leva N ( \_ iQueueDelay variável no código de exemplo) número de chamadas presentes em que N (g \_ iQueueDelay) é igual a g \_ iImmediates mais o comprimento da fila atual, ou seja:</span><span class="sxs-lookup"><span data-stu-id="53ecd-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="53ecd-268">Ignorando quadros com o intervalo atual D3DPRESENT \_ FORCEIMMEDIATE, além de</span><span class="sxs-lookup"><span data-stu-id="53ecd-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="53ecd-269">Presentes na fila que precisam ser processados</span><span class="sxs-lookup"><span data-stu-id="53ecd-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="53ecd-270">Defina um limite para o comprimento da falha ( \_ limite de recuperação \_ de falha em exemplo).</span><span class="sxs-lookup"><span data-stu-id="53ecd-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="53ecd-271">Se o aplicativo de exemplo não puder se recuperar de uma falha que seja muito longa (ou seja, 1 segundo ou 60 vsyncs no monitor de 60 Hz), pule a animação intermitente e redefina a fila do auxiliar atual.</span><span class="sxs-lookup"><span data-stu-id="53ecd-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="53ecd-272">**Cenário de exemplo**</span><span class="sxs-lookup"><span data-stu-id="53ecd-272">**Sample scenario**</span></span>

-   <span data-ttu-id="53ecd-273">A ilustração a seguir mostra um aplicativo com a contagem de backbuffers de 4.</span><span class="sxs-lookup"><span data-stu-id="53ecd-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="53ecd-274">O comprimento real da fila atual é, portanto, 5.</span><span class="sxs-lookup"><span data-stu-id="53ecd-274">The actual Present queue length is therefore 5.</span></span>

    ![ilustração de um applicas de quadros renderizados e da fila presente](images/sample-scenario.png)

    <span data-ttu-id="53ecd-276">O quadro A é direcionado para entrar na tela na contagem de intervalos de sincronização de 1, mas foi detectado que foi mostrado na contagem de intervalos de sincronização de 4.</span><span class="sxs-lookup"><span data-stu-id="53ecd-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="53ecd-277">Portanto, ocorreu um problema.</span><span class="sxs-lookup"><span data-stu-id="53ecd-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="53ecd-278">Três quadros subsequentes são apresentados com o intervalo de D3DPRESENT \_ \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="53ecd-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="53ecd-279">A falha deve levar um total de 8 chamadas presentes antes de ser recuperada-o próximo quadro será mostrado de acordo com sua contagem de intervalos de sincronização de destino.</span><span class="sxs-lookup"><span data-stu-id="53ecd-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="53ecd-280">Resumo das recomendações de programação para sincronização de quadros</span><span class="sxs-lookup"><span data-stu-id="53ecd-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="53ecd-281">Crie uma lista de backup de todas as IDs de LastPresentCount (obtidas via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) e a PresentRefreshCount estimada associada de todos os presentes enviados.</span><span class="sxs-lookup"><span data-stu-id="53ecd-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="53ecd-282">Quando o aplicativo chama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT \_ DONOTFLIP, a chamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é realizada com sucesso, mas não retorna uma estrutura de [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="53ecd-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="53ecd-283">Chame [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obter o PresentRefreshCount real associado a cada ID presente de quadros mostrados, para garantir que o aplicativo manipule as Devoluções de falha da chamada.</span><span class="sxs-lookup"><span data-stu-id="53ecd-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="53ecd-284">Se o PresentRefreshCount real for posterior ao PresentRefreshCount estimado, um problema será detectado.</span><span class="sxs-lookup"><span data-stu-id="53ecd-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="53ecd-285">Compensar enviando quadros de retardo "presentes com D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="53ecd-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="53ecd-286">Quando um quadro é apresentado tardiamente na fila atual, todos os quadros em fila subsequentes serão apresentados em atraso.</span><span class="sxs-lookup"><span data-stu-id="53ecd-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="53ecd-287">D3DPRESENT \_ FORCEIMMEDIATE corrigirá apenas o próximo quadro a ser apresentado após todos os quadros em fila.</span><span class="sxs-lookup"><span data-stu-id="53ecd-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="53ecd-288">Portanto, a contagem de fila atual ou de BackBuffer não deve ser muito longa. portanto, há menos falhas de quadro para acompanhar.</span><span class="sxs-lookup"><span data-stu-id="53ecd-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="53ecd-289">A contagem de BackBuffer ideal é de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="53ecd-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="53ecd-290">Se o PresentRefreshCount estimado for posterior ao PresentRefreshCount real, a limitação do DWM poderá ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="53ecd-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="53ecd-291">As seguintes soluções são possíveis:</span><span class="sxs-lookup"><span data-stu-id="53ecd-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="53ecd-292">reduzindo o tamanho da fila atual</span><span class="sxs-lookup"><span data-stu-id="53ecd-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="53ecd-293">reduzir os requisitos de memória da GPU com outros meios além de reduzir o tamanho da fila atual (ou seja, diminuir a qualidade, remover efeitos e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="53ecd-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="53ecd-294">especificando [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) para evitar a limitação do DWM em geral</span><span class="sxs-lookup"><span data-stu-id="53ecd-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="53ecd-295">Verifique a funcionalidade de exibição do aplicativo e o desempenho de estatísticas do quadro nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="53ecd-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="53ecd-296">com o DWM ligado e desligado</span><span class="sxs-lookup"><span data-stu-id="53ecd-296">with DWM on and off</span></span>
    -   <span data-ttu-id="53ecd-297">modo de tela inteira e modos de janela</span><span class="sxs-lookup"><span data-stu-id="53ecd-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="53ecd-298">hardware de funcionalidade inferior</span><span class="sxs-lookup"><span data-stu-id="53ecd-298">lower capability hardware</span></span>

-   <span data-ttu-id="53ecd-299">Quando os aplicativos não podem se recuperar de grandes números de quadros com falha com D3DPRESENT \_ FORCEIMMEDIATE presente, eles podem potencialmente executar as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="53ecd-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="53ecd-300">Reduza o uso de CPU e GPU ao renderizar com menos carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="53ecd-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="53ecd-301">no caso de decodificação de vídeo, decodificação mais rápido reduzindo a qualidade e, portanto, o uso de CPU e GPU.</span><span class="sxs-lookup"><span data-stu-id="53ecd-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="53ecd-302">Conclusão sobre os aprimoramentos do Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="53ecd-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="53ecd-303">No Windows 7, os aplicativos que exibem a taxa de quadros de vídeo ou medidor durante a apresentação podem optar pelo flip Model.</span><span class="sxs-lookup"><span data-stu-id="53ecd-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="53ecd-304">Os aprimoramentos de estatísticas atuais que estão associados ao flip Model Direct3D 9Ex podem beneficiar os aplicativos que sincronizam a apresentação por taxa de quadros, com comentários em tempo real para detecção e recuperação de problemas.</span><span class="sxs-lookup"><span data-stu-id="53ecd-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="53ecd-305">Os desenvolvedores que adotam o modelo do Direct3D 9Ex flip devem ter como destino um HWND separado do conteúdo do GDI e da sincronização de taxa de quadros em conta.</span><span class="sxs-lookup"><span data-stu-id="53ecd-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="53ecd-306">Consulte os detalhes neste tópico e a documentação do MSDN.</span><span class="sxs-lookup"><span data-stu-id="53ecd-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="53ecd-307">Para obter mais documentação, consulte [DirectX Developer Center no MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="53ecd-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="53ecd-308">Plano de ação</span><span class="sxs-lookup"><span data-stu-id="53ecd-308">Call to Action</span></span>

<span data-ttu-id="53ecd-309">Incentivamos você a usar o modelo de inversão do Direct3D 9Ex e suas estatísticas atuais no Windows 7 ao criar aplicativos que tentam sincronizar a taxa de quadros de apresentação ou se recuperar de falhas de exibição.</span><span class="sxs-lookup"><span data-stu-id="53ecd-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53ecd-310">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53ecd-310">Related topics</span></span>

<span data-ttu-id="53ecd-311">[Central de desenvolvedores do DirectX no MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="53ecd-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>