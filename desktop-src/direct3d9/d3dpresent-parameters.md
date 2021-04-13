---
description: Descreve os parâmetros de apresentação.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Estrutura de D3DPRESENT_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298661"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="16641-103">\_Estrutura de parâmetros D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="16641-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="16641-104">Descreve os parâmetros de apresentação.</span><span class="sxs-lookup"><span data-stu-id="16641-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="16641-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16641-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="16641-106">Membros</span><span class="sxs-lookup"><span data-stu-id="16641-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="16641-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="16641-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="16641-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-109">Largura dos buffers de fundo da nova cadeia de permuta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="16641-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="16641-110">Se a **janela** for **false** (a apresentação é de tela inteira), esse valor deverá ser igual à largura de um dos modos de exibição enumerados encontrados por meio de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="16641-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="16641-111">Se a **janela** for **true** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área do cliente do **hDeviceWindow** (ou a janela de foco se **hDeviceWindow** for **NULL**) será executada.</span><span class="sxs-lookup"><span data-stu-id="16641-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="16641-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="16641-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="16641-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-114">Altura dos buffers de fundo da nova cadeia de permuta, em pixels.</span><span class="sxs-lookup"><span data-stu-id="16641-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="16641-115">Se a **janela** for **false** (a apresentação é de tela inteira), esse valor deverá ser igual à altura de um dos modos de exibição enumerados encontrados por meio de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="16641-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="16641-116">Se a **janela** for **true** e **BackBufferWidth** ou **BackBufferHeight** for zero, a dimensão correspondente da área do cliente do **hDeviceWindow** (ou a janela de foco se **hDeviceWindow** for **NULL**) será executada.</span><span class="sxs-lookup"><span data-stu-id="16641-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="16641-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="16641-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="16641-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-119">O formato de buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="16641-119">The back buffer format.</span></span> <span data-ttu-id="16641-120">Para obter mais informações sobre formatos, consulte [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="16641-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="16641-121">Esse valor deve ser um dos formatos de destino de renderização como validado por [**CheckDeviceType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="16641-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="16641-122">Você pode usar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) para obter o formato atual.</span><span class="sxs-lookup"><span data-stu-id="16641-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="16641-123">Na verdade, D3DFMT \_ Unknown pode ser especificado para o **BackBufferFormat** enquanto estiver no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="16641-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="16641-124">Isso informa o tempo de execução para usar o formato atual do modo de exibição e elimina a necessidade de chamar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="16641-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="16641-125">Para aplicativos em janelas, o formato de buffer de fundo não precisa mais corresponder ao formato de modo de exibição porque a conversão de cores agora pode ser feita pelo hardware (se o hardware oferecer suporte à conversão de cores).</span><span class="sxs-lookup"><span data-stu-id="16641-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="16641-126">O conjunto de possíveis formatos de buffer de fundo é restrito, mas o tempo de execução permitirá que qualquer formato de buffer de fundo válido seja apresentado a qualquer formato de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="16641-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="16641-127">(Há o requisito adicional de que o dispositivo seja operável na área de trabalho; os dispositivos normalmente não operam em 8 bits por modo de pixel.)</span><span class="sxs-lookup"><span data-stu-id="16641-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="16641-128">Os aplicativos de tela inteira não podem fazer a conversão de cores.</span><span class="sxs-lookup"><span data-stu-id="16641-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="16641-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="16641-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="16641-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-131">Esse valor pode ter entre 0 e [D3DPRESENT \_ \_ buffers de fundo \_ máximo](d3dpresent-back-buffers.md) (ou [D3DPRESENT \_ buffers de back-Max, por \_ \_ \_ exemplo](d3dpresent-back-buffers.md) , ao usar o Direct3D 9EX).</span><span class="sxs-lookup"><span data-stu-id="16641-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="16641-132">Os valores de 0 são tratados como 1.</span><span class="sxs-lookup"><span data-stu-id="16641-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="16641-133">Se o número de buffers de fundo não puder ser criado, o tempo de execução falhará na chamada de método e preencherá esse valor com o número de buffers de fundo que podem ser criados.</span><span class="sxs-lookup"><span data-stu-id="16641-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="16641-134">Como resultado, um aplicativo pode chamar o método duas vezes com a mesma \_ estrutura de parâmetros D3DPRESENT e esperar que ela funcione na segunda vez.</span><span class="sxs-lookup"><span data-stu-id="16641-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="16641-135">O método falhará se não for possível criar um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="16641-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="16641-136">O valor de **BackBufferCount** influencia o conjunto de efeitos de permuta permitido.</span><span class="sxs-lookup"><span data-stu-id="16641-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="16641-137">Especificamente, qualquer \_ efeito de troca de cópia D3DSWAPEFFECT requer que haja exatamente um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="16641-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="16641-138">**Multiamostratype**</span><span class="sxs-lookup"><span data-stu-id="16641-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="16641-139">Tipo: **[ **\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-140">Membro do tipo enumerado do [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="16641-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="16641-141">O valor deve ser D3DMULTISAMPLE \_ nenhum, a menos que **SwapEffect** tenha sido definido como \_ descartar D3DSWAPEFFECT.</span><span class="sxs-lookup"><span data-stu-id="16641-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="16641-142">Haverá suporte para multiamostrar apenas se o efeito de permuta for D3DSWAPEFFECT \_ descartar.</span><span class="sxs-lookup"><span data-stu-id="16641-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="16641-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="16641-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="16641-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-145">Nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="16641-145">Quality level.</span></span> <span data-ttu-id="16641-146">O intervalo válido é entre zero e um menor que o nível retornado por pQualityLevels usado pelo [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="16641-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="16641-147">Passar um valor maior retorna o erro D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="16641-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="16641-148">Valores emparelhados de destinos de renderização ou de superfícies de estêncil de profundidade e [**\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md) devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="16641-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="16641-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="16641-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="16641-150">Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-151">Membro do tipo enumerado [**D3DSWAPEFFECT**](./d3dswapeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="16641-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="16641-152">O tempo de execução garantirá a semântica implícita relacionada ao comportamento de permuta no buffer; Portanto, se a **janela** for **true** e **SwapEffect** for definido como D3DSWAPEFFECT \_ flip, o tempo de execução criará um buffer de fundo extra e copiará o que for o buffer frontal no momento da apresentação.</span><span class="sxs-lookup"><span data-stu-id="16641-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="16641-153">D3DSWAPEFFECT \_ Copy requer que **BackBufferCount** seja definido como 1.</span><span class="sxs-lookup"><span data-stu-id="16641-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="16641-154">\_O descarte de D3DSWAPEFFECT será imposto no tempo de execução de depuração preenchendo qualquer buffer com ruído depois que ele for apresentado.</span><span class="sxs-lookup"><span data-stu-id="16641-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16641-155">Diferenças entre o Direct3D9 e o Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="16641-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="16641-156">Em Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX é adicionado para designar quando um aplicativo está adotando o modo flip.</span><span class="sxs-lookup"><span data-stu-id="16641-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="16641-157">Ou seja, Whan o quadro de um aplicativo é passado no modo da janela (em vez de copiado) para o Gerenciador de Janelas da Área de Trabalho (DWM) para composição.</span><span class="sxs-lookup"><span data-stu-id="16641-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="16641-158">O modo Inverter fornece largura de banda de memória mais eficiente e permite que um aplicativo aproveite as estatísticas de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="16641-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="16641-159">Ele não altera o comportamento de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="16641-159">It does not change full screen behavior.</span></span> <span data-ttu-id="16641-160">O comportamento do modo flip está disponível a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16641-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="16641-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="16641-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="16641-162">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-163">A janela do dispositivo determina o local e o tamanho do buffer de fundo na tela.</span><span class="sxs-lookup"><span data-stu-id="16641-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="16641-164">Isso é usado pelo Direct3D quando o conteúdo do buffer de fundo é copiado para o buffer frontal durante a [**apresentação**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="16641-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="16641-165">Para um aplicativo de tela inteira, trata-se de um identificador para a janela superior (que é a janela de foco).</span><span class="sxs-lookup"><span data-stu-id="16641-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="16641-166">Para aplicativos que usam vários dispositivos de tela inteira (como um sistema multimonitor), exatamente um dispositivo pode usar a janela de foco como a janela do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16641-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="16641-167">Todos os outros dispositivos devem ter janelas de dispositivo exclusivas.</span><span class="sxs-lookup"><span data-stu-id="16641-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="16641-168">Para um aplicativo em modo de janela, esse identificador será a janela de destino padrão para o [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="16641-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="16641-169">Se esse identificador for **nulo**, a janela de foco será tomada.</span><span class="sxs-lookup"><span data-stu-id="16641-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="16641-170">Observe que nenhuma tentativa é feita pelo tempo de execução para refletir as alterações do usuário no tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="16641-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="16641-171">O buffer de fundo não é implicitamente redefinido quando esta janela é redefinida.</span><span class="sxs-lookup"><span data-stu-id="16641-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="16641-172">No entanto, o método [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) controla automaticamente as alterações na posição da janela.</span><span class="sxs-lookup"><span data-stu-id="16641-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="16641-173">**Em janelas**</span><span class="sxs-lookup"><span data-stu-id="16641-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="16641-174">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-175">**True** se o aplicativo for executado em janela; **False** se o aplicativo for executado em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="16641-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="16641-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="16641-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="16641-177">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-178">Se esse valor for **true**, o Direct3D gerenciará buffers de profundidade para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16641-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="16641-179">O dispositivo criará um buffer de estêncil de profundidade quando for criado.</span><span class="sxs-lookup"><span data-stu-id="16641-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="16641-180">O buffer de estêncil de profundidade será definido automaticamente como o destino de renderização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16641-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="16641-181">Quando o dispositivo for redefinido, o buffer de estêncil de profundidade será automaticamente destruído e recriado no novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="16641-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="16641-182">Se EnableAutoDepthStencil for **true**, AutoDepthStencilFormat deverá ser um formato de estêncil de profundidade válido.</span><span class="sxs-lookup"><span data-stu-id="16641-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="16641-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="16641-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="16641-184">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-185">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="16641-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="16641-186">O formato da superfície de estêncil de profundidade automática que o dispositivo criará.</span><span class="sxs-lookup"><span data-stu-id="16641-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="16641-187">Esse membro é ignorado, a menos que **EnableAutoDepthStencil** seja **true**.</span><span class="sxs-lookup"><span data-stu-id="16641-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="16641-188">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="16641-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="16641-189">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-190">Uma das constantes [D3DPRESENTFLAG](d3dpresentflag.md) .</span><span class="sxs-lookup"><span data-stu-id="16641-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="16641-191">**Tela inteira \_ RefreshRateInHz**</span><span class="sxs-lookup"><span data-stu-id="16641-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="16641-192">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-193">A taxa na qual o adaptador de vídeo atualiza a tela.</span><span class="sxs-lookup"><span data-stu-id="16641-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="16641-194">O valor depende do modo no qual o aplicativo está em execução:</span><span class="sxs-lookup"><span data-stu-id="16641-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="16641-195">Para o modo em janela, a taxa de atualização deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="16641-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="16641-196">Para o modo de tela inteira, a taxa de atualização é uma das taxas de atualização retornadas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="16641-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="16641-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="16641-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="16641-198">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16641-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16641-199">A taxa máxima na qual os buffers de fundo da cadeia de troca podem ser apresentados ao buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="16641-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="16641-200">Para obter uma explicação detalhada dos modos e dos intervalos com suporte, consulte [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="16641-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16641-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16641-201">Requirements</span></span>



| <span data-ttu-id="16641-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="16641-202">Requirement</span></span> | <span data-ttu-id="16641-203">Valor</span><span class="sxs-lookup"><span data-stu-id="16641-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16641-204">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16641-204">Header</span></span><br/> | <dl> <span data-ttu-id="16641-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="16641-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16641-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="16641-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16641-207">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="16641-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="16641-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="16641-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="16641-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="16641-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="16641-210">**Existi**</span><span class="sxs-lookup"><span data-stu-id="16641-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="16641-211">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="16641-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
