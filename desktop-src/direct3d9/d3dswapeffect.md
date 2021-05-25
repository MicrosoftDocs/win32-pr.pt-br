---
description: Define efeitos de permuta.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Enumeração D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343031"
---
# <a name="d3dswapeffect-enumeration"></a><span data-ttu-id="f952a-103">Enumeração D3DSWAPEFFECT</span><span class="sxs-lookup"><span data-stu-id="f952a-103">D3DSWAPEFFECT enumeration</span></span>

<span data-ttu-id="f952a-104">Define efeitos de permuta.</span><span class="sxs-lookup"><span data-stu-id="f952a-104">Defines swap effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="f952a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f952a-105">Syntax</span></span>

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a><span data-ttu-id="f952a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f952a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f952a-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ DISCARD**</span><span class="sxs-lookup"><span data-stu-id="f952a-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT\_DISCARD**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-108">Quando uma cadeia de permuta é criada com um efeito de permuta de D3DSWAPEFFECT FLIP ou \_ D3DSWAPEFFECT COPY, o runtime garantirá que uma \_ operação [**IDirect3DDevice9::P resent**](/windows/desktop/api) não afetará o conteúdo de nenhum dos buffers de fundo.</span><span class="sxs-lookup"><span data-stu-id="f952a-108">When a swap chain is created with a swap effect of D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_COPY, the runtime will guarantee that an [**IDirect3DDevice9::Present**](/windows/desktop/api) operation will not affect the content of any of the back buffers.</span></span> <span data-ttu-id="f952a-109">Infelizmente, atender a essa garantia pode envolver sobrecargas substanciais de processamento ou memória de vídeo, especialmente ao implementar semântica de invasões para uma cadeia de permuta em janelas ou semântica de cópia para uma cadeia de permuta de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="f952a-109">Unfortunately, meeting this guarantee can involve substantial video memory or processing overheads, especially when implementing flip semantics for a windowed swap chain or copy semantics for a full-screen swap chain.</span></span> <span data-ttu-id="f952a-110">Um aplicativo pode usar o efeito de troca D3DSWAPEFFECT DISCARD para evitar essas sobrecargas e permitir que o driver de exibição selecione a técnica de apresentação mais eficiente para a cadeia \_ de permuta.</span><span class="sxs-lookup"><span data-stu-id="f952a-110">An application may use the D3DSWAPEFFECT\_DISCARD swap effect to avoid these overheads and to enable the display driver to select the most efficient presentation technique for the swap chain.</span></span> <span data-ttu-id="f952a-111">Esse também é o único efeito de permuta que pode ser usado ao especificar um valor diferente de D3DMULTISAMPLE NONE para o membro \_ MultiSampleType [**de D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f952a-111">This is also the only swap effect that may be used when specifying a value other than D3DMULTISAMPLE\_NONE for the MultiSampleType member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="f952a-112">Como uma cadeia de permuta que usa D3DSWAPEFFECT FLIP, uma cadeia de permuta que usa D3DSWAPEFFECT DISCARD pode incluir mais de um buffer de retorno, qualquer um deles pode ser acessado usando \_ \_ [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) ou [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer).</span><span class="sxs-lookup"><span data-stu-id="f952a-112">Like a swap chain that uses D3DSWAPEFFECT\_FLIP, a swap chain that uses D3DSWAPEFFECT\_DISCARD might include more than one back buffer, any of which may be accessed using [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) or [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer).</span></span> <span data-ttu-id="f952a-113">A cadeia de permuta é melhor prevista como uma fila na qual 0 sempre indexa o buffer de fundo que será exibido pela próxima operação Presente e da qual os buffers serão descartados quando eles foram exibidos.</span><span class="sxs-lookup"><span data-stu-id="f952a-113">The swap chain is best envisaged as a queue in which 0 always indexes the back buffer that will be displayed by the next Present operation and from which buffers are discarded when they have been displayed.</span></span>

<span data-ttu-id="f952a-114">Um aplicativo que usa esse efeito de permuta não pode fazer suposições sobre o conteúdo de um buffer de fundo descartado e, portanto, deve atualizar um buffer de fundo inteiro antes de invocar uma operação Present que o exibiria.</span><span class="sxs-lookup"><span data-stu-id="f952a-114">An application that uses this swap effect cannot make any assumptions about the contents of a discarded back buffer and should therefore update an entire back buffer before invoking a Present operation that would display it.</span></span> <span data-ttu-id="f952a-115">Embora isso não seja imposto, a versão de depuração do runtime substituirá o conteúdo dos buffers de fundo descartados por dados aleatórios para permitir que os desenvolvedores verifiquem se seus aplicativos estão atualizando todas as superfícies do buffer de fundo corretamente.</span><span class="sxs-lookup"><span data-stu-id="f952a-115">Although this is not enforced, the debug version of the runtime will overwrite the contents of discarded back buffers with random data to enable developers to verify that their applications are updating the entire back buffer surfaces correctly.</span></span>

</dd> <dt>

<span data-ttu-id="f952a-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**</span><span class="sxs-lookup"><span data-stu-id="f952a-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT\_FLIP**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-117">A cadeia de permuta pode incluir vários buffers de fundo e é a melhor previu como uma fila circular que inclui o buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="f952a-117">The swap chain might include multiple back buffers and is best envisaged as a circular queue that includes the front buffer.</span></span> <span data-ttu-id="f952a-118">Nessa fila, os buffers traseiros são sempre numerados sequencialmente de 0 a (n-1), em que n é o número de buffers de fundo, de modo que 0 denota o buffer apresentado menos recentemente.</span><span class="sxs-lookup"><span data-stu-id="f952a-118">Within this queue, the back buffers are always numbered sequentially from 0 to (n - 1), where n is the number of back buffers, so that 0 denotes the least recently presented buffer.</span></span> <span data-ttu-id="f952a-119">Quando presente é invocado, a fila é "girada" para que o buffer frontal se torne buffer (n-1), enquanto o buffer de fundo 0 se torna o novo buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="f952a-119">When Present is invoked, the queue is "rotated" so that the front buffer becomes back buffer (n - 1), while the back buffer 0 becomes the new front buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f952a-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**\_Cópia D3DSWAPEFFECT**</span><span class="sxs-lookup"><span data-stu-id="f952a-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-121">Esse efeito de permuta pode ser especificado apenas para uma cadeia de permuta que contém um único buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="f952a-121">This swap effect may be specified only for a swap chain comprising a single back buffer.</span></span> <span data-ttu-id="f952a-122">Se a cadeia de permuta estiver em janela ou em tela inteira, o tempo de execução garantirá a semântica implícita por uma operação presente com base em cópia, ou seja, a operação deixa o conteúdo do buffer de fundo inalterado, em vez de substituí-lo pelo conteúdo do buffer frontal como uma operação presente com base em inversão.</span><span class="sxs-lookup"><span data-stu-id="f952a-122">Whether the swap chain is windowed or full-screen, the runtime will guarantee the semantics implied by a copy-based Present operation, namely that the operation leaves the content of the back buffer unchanged, instead of replacing it with the content of the front buffer as a flip-based Present operation would.</span></span>

<span data-ttu-id="f952a-123">Para uma cadeia de troca de tela inteira, o tempo de execução usa uma combinação de operações de inversão e operações de cópia, com suporte se necessário pelos buffers de fundo ocultos, para realizar a operação atual.</span><span class="sxs-lookup"><span data-stu-id="f952a-123">For a full-screen swap chain, the runtime uses a combination of flip operations and copy operations, supported if necessary by hidden back buffers, to accomplish the Present operation.</span></span> <span data-ttu-id="f952a-124">Da mesma forma, a apresentação é sincronizada com o rerastreamento vertical do adaptador de vídeo e sua taxa é restrita pelo intervalo de apresentação escolhido.</span><span class="sxs-lookup"><span data-stu-id="f952a-124">Accordingly, the presentation is synchronized with the display adapter's vertical retrace and its rate is constrained by the chosen presentation interval.</span></span> <span data-ttu-id="f952a-125">Uma cadeia de permuta especificada com o \_ sinalizador Immediate de intervalo de D3DPRESENT \_ é a única exceção.</span><span class="sxs-lookup"><span data-stu-id="f952a-125">A swap chain specified with the D3DPRESENT\_INTERVAL\_IMMEDIATE flag is the only exception.</span></span> <span data-ttu-id="f952a-126">(Consulte a descrição do membro **PresentationIntervals** da estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) .) Nesse caso, uma operação atual copia o conteúdo do buffer de fundo diretamente para o buffer frontal sem aguardar o rerastreamento vertical.</span><span class="sxs-lookup"><span data-stu-id="f952a-126">(Refer to the description of the **PresentationIntervals** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure.) In this case, a Present operation copies the back buffer content directly to the front buffer without waiting for the vertical retrace.</span></span>

</dd> <dt>

<span data-ttu-id="f952a-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**Sobreposição de D3DSWAPEFFECT \_**</span><span class="sxs-lookup"><span data-stu-id="f952a-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT\_OVERLAY**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-128">Use uma área dedicada de memória de vídeo que possa ser sobreposta na superfície primária.</span><span class="sxs-lookup"><span data-stu-id="f952a-128">Use a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="f952a-129">Nenhuma cópia é executada quando a sobreposição é exibida.</span><span class="sxs-lookup"><span data-stu-id="f952a-129">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="f952a-130">A operação de sobreposição é executada no hardware, sem modificar os dados na superfície primária.</span><span class="sxs-lookup"><span data-stu-id="f952a-130">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="f952a-131">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="f952a-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="f952a-132">D3DSWAPEFFECT OVERLAY só está disponível no Direct3D9Ex em execução no \_ Windows 7 (ou sistema operacional mais atual).</span><span class="sxs-lookup"><span data-stu-id="f952a-132">D3DSWAPEFFECT\_OVERLAY is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>

</dd> <dt>

<span data-ttu-id="f952a-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**</span><span class="sxs-lookup"><span data-stu-id="f952a-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT\_FLIPEX**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-134">Designa quando um aplicativo está adotando o modo de in flip, durante o qual o quadro de um aplicativo é passado em vez de copiado para o DWM (Gerenciador de Janelas da Área de Trabalho) para composição quando o aplicativo está apresentando no modo em janelas.</span><span class="sxs-lookup"><span data-stu-id="f952a-134">Designates when an application is adopting flip mode, during which time an application's frame is passed instead of copied to the Desktop Window Manager(DWM) for composition when the application is presenting in windowed mode.</span></span> <span data-ttu-id="f952a-135">O modo de invasão permite que um aplicativo use com mais eficiência a largura de banda de memória, além de permitir que um aplicativo aproveite as estatísticas de tela inteira presentes.</span><span class="sxs-lookup"><span data-stu-id="f952a-135">Flip mode allows an application to more efficiently use memory bandwidth as well as enabling an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="f952a-136">O modo de in flip não afeta o comportamento de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="f952a-136">Flip mode does not affect full-screen behavior.</span></span>

> [!Note]  
> <span data-ttu-id="f952a-137">Se você criar uma cadeia de permuta com D3DSWAPEFFECT FLIPEX, não poderá substituir o \_ **membro hDeviceWindow** da estrutura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) quando apresentar um novo quadro para exibição.</span><span class="sxs-lookup"><span data-stu-id="f952a-137">If you create a swap chain with D3DSWAPEFFECT\_FLIPEX, you can't override the **hDeviceWindow** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure when you present a new frame for display.</span></span> <span data-ttu-id="f952a-138">Ou seja, você deve passar **NULL** para o parâmetro *hDestWindowOverride* [**de IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) para instruir o runtime a usar o **membro hDeviceWindow** **de D3DPRESENT \_ PARAMETERS** para a apresentação.</span><span class="sxs-lookup"><span data-stu-id="f952a-138">That is, you must pass **NULL** to the *hDestWindowOverride* parameter of [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) to instruct the runtime to use the **hDeviceWindow** member of **D3DPRESENT\_PARAMETERS** for the presentation.</span></span>

<span data-ttu-id="f952a-139">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="f952a-139">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="f952a-140">D3DSWAPEFFECT FLIPEX só está disponível no Direct3D9Ex em execução no \_ Windows 7 (ou sistema operacional mais atual).</span><span class="sxs-lookup"><span data-stu-id="f952a-140">D3DSWAPEFFECT\_FLIPEX is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>

</dd> <dt>

<span data-ttu-id="f952a-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f952a-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f952a-142">Força essa enumeração a compilar para 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="f952a-142">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f952a-143">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f952a-143">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f952a-144">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="f952a-144">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f952a-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="f952a-145">Remarks</span></span>

<span data-ttu-id="f952a-146">O estado do buffer de fundo após uma chamada para Present é bem definido por cada um desses efeitos de permuta e se o dispositivo Direct3D foi criado com uma cadeia de permuta de tela inteira ou uma cadeia de permuta em janelas não tem efeito sobre esse estado.</span><span class="sxs-lookup"><span data-stu-id="f952a-146">The state of the back buffer after a call to Present is well-defined by each of these swap effects, and whether the Direct3D device was created with a full-screen swap chain or a windowed swap chain has no effect on this state.</span></span> <span data-ttu-id="f952a-147">Em particular, o efeito de troca FLIP D3DSWAPEFFECT opera da mesma forma, seja em janelas ou em tela inteira, e o runtime do Direct3D garante isso criando \_ buffers extras.</span><span class="sxs-lookup"><span data-stu-id="f952a-147">In particular, the D3DSWAPEFFECT\_FLIP swap effect operates the same whether windowed or full-screen, and the Direct3D runtime guarantees this by creating extra buffers.</span></span> <span data-ttu-id="f952a-148">Como resultado, é recomendável que os aplicativos usem D3DSWAPEFFECT DISCARD sempre que possível para \_ evitar tais penalidades.</span><span class="sxs-lookup"><span data-stu-id="f952a-148">As a result, it is recommended that applications use D3DSWAPEFFECT\_DISCARD whenever possible to avoid any such penalties.</span></span> <span data-ttu-id="f952a-149">Isso ocorre porque esse efeito de permuta será sempre o mais eficiente em termos de desempenho e consumo de memória.</span><span class="sxs-lookup"><span data-stu-id="f952a-149">This is because this swap effect will always be the most efficient in terms of memory consumption and performance.</span></span>

<span data-ttu-id="f952a-150">Os aplicativos que usam D3DSWAPEFFECT \_ inverter ou D3DSWAPEFFECT \_ descartar não devem esperar que o destino de tela inteira funcione.</span><span class="sxs-lookup"><span data-stu-id="f952a-150">Applications that use D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD should not expect full-screen destination alpha to work.</span></span> <span data-ttu-id="f952a-151">Isso significa que o \_ estado de RENDERIZAÇÃO D3DRS DESTBLEND não funcionará conforme o esperado porque as cadeias de troca de tela inteira com esses efeitos de permuta não têm um formato de pixel explícito do ponto de vista do driver.</span><span class="sxs-lookup"><span data-stu-id="f952a-151">This means that the D3DRS\_DESTBLEND render state will not work as expected because full-screen swap chains with these swap effects do not have an explicit pixel format from the driver's point of view.</span></span> <span data-ttu-id="f952a-152">O driver infere que eles devem assumir o formato de exibição, que não tem um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="f952a-152">The driver infers that they should take on the display format, which does not have an alpha channel.</span></span> <span data-ttu-id="f952a-153">Para contornar isso, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="f952a-153">To work around this, take the following steps:</span></span>

-   <span data-ttu-id="f952a-154">Use a \_ cópia D3DSWAPEFFECT.</span><span class="sxs-lookup"><span data-stu-id="f952a-154">Use D3DSWAPEFFECT\_COPY.</span></span>
-   <span data-ttu-id="f952a-155">Verifique o \_ \_ \_ \_ sinalizador flip ou Discard D3DCAPS3 Alpha fullscreen \_ no membro Caps3 da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="f952a-155">Check the D3DCAPS3\_ALPHA\_FULLSCREEN\_FLIP\_OR\_DISCARD flag in the Caps3 member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="f952a-156">Esse sinalizador indica se o driver pode fazer a mesclagem alfa quando D3DSWAPEFFECT \_ flip ou D3DSWAPEFFECT \_ descartável é usado.</span><span class="sxs-lookup"><span data-stu-id="f952a-156">This flag indicates whether the driver can do alpha blending when D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD is used.</span></span>
-   <span data-ttu-id="f952a-157">Os aplicativos que usam o efeito de permuta do modo flip (D3DSWAPEFFECT \_ FLIPEX) devem chamar [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) após uma alteração de região ou redimensionamento de janela para garantir que o conteúdo de exibição seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="f952a-157">Applications using flip mode swap effect (D3DSWAPEFFECT\_FLIPEX) should call [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) after a window resize or region change to ensure that the display content is updated.</span></span>

<span data-ttu-id="f952a-158">Uma janela invisível não pode receber eventos de modo de usuário; Além disso, uma janela invisível-fullscreen interfere na apresentação da janela de modo em janela de outra aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f952a-158">An invisible window cannot receive user-mode events; furthermore, an invisible-fullscreen window will interfere with the presentation of another applications' windowed-mode window.</span></span> <span data-ttu-id="f952a-159">Portanto, cada aplicativo precisa garantir que uma janela de dispositivo esteja visível quando um SwapChain é apresentado no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="f952a-159">Therefore, each application needs to ensure that a device window is visible when a swapchain is presented in fullscreen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="f952a-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f952a-160">Requirements</span></span>

| <span data-ttu-id="f952a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="f952a-161">Requirement</span></span> | <span data-ttu-id="f952a-162">Valor</span><span class="sxs-lookup"><span data-stu-id="f952a-162">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f952a-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f952a-163">Header</span></span><br/> | <dl> <span data-ttu-id="f952a-164"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f952a-164"><dt>D3D9Types.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="f952a-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="f952a-165">See also</span></span>

[<span data-ttu-id="f952a-166">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f952a-166">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)

[<span data-ttu-id="f952a-167">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="f952a-167">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
