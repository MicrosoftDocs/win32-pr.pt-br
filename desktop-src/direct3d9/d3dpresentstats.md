---
description: Descreve as estatísticas de SwapChain relacionadas a chamadas PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Estrutura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173054"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="3ed6b-103">Estrutura D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="3ed6b-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="3ed6b-104">Descreve as estatísticas de SwapChain relacionadas a chamadas [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="3ed6b-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed6b-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="3ed6b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3ed6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ed6b-107">**PresentCount**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="3ed6b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ed6b-109">Contagem em execução de chamadas presentes bem-sucedidas feitas por um dispositivo de vídeo que está sendo disponibilizado para a tela.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="3ed6b-110">Esse parâmetro é realmente a ID atual da última chamada presente e não é necessariamente o número total de chamadas de API presentes.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="3ed6b-111">**PresentRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="3ed6b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ed6b-113">A contagem de vblank em que a última apresentação foi exibida na tela, a contagem de vblank é incrementada uma vez a cada intervalo de vblank.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="3ed6b-114">**SyncRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="3ed6b-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ed6b-116">A contagem de vblank quando o Agendador último amostra a hora da máquina chamando QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="3ed6b-117">**SyncQPCTime**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="3ed6b-118">Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="3ed6b-119">A última hora da máquina de amostra do Agendador, obtida com a chamada de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="3ed6b-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="3ed6b-120">**SyncGPUTime**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="3ed6b-121">Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="3ed6b-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="3ed6b-122">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ed6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed6b-123">Remarks</span></span>

<span data-ttu-id="3ed6b-124">Quando um aplicativo 9Ex adota o modo invertido presente (D3DSWAPEFFECT \_ FLIPEX), os aplicativos podem detectar o descarte de quadros chamando GetPresentStatistics em qualquer ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="3ed6b-125">Na verdade, eles podem fazer o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="3ed6b-126">Renderizar para o buffer de fundo</span><span class="sxs-lookup"><span data-stu-id="3ed6b-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="3ed6b-127">Chamada presente</span><span class="sxs-lookup"><span data-stu-id="3ed6b-127">Call Present</span></span>
3.  <span data-ttu-id="3ed6b-128">Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="3ed6b-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="3ed6b-129">Renderizar o próximo quadro para o buffer de fundo</span><span class="sxs-lookup"><span data-stu-id="3ed6b-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="3ed6b-130">Chamada presente</span><span class="sxs-lookup"><span data-stu-id="3ed6b-130">Call Present</span></span>
6.  <span data-ttu-id="3ed6b-131">Repita as etapas 4 e 5 1 ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="3ed6b-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="3ed6b-132">Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="3ed6b-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="3ed6b-133">Compare os valores de PresentRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="3ed6b-134">O aplicativo pode calcular o PresentRefreshCount correspondente de um parâmetro PresentCount específico com base nas suposições do incremento de PresentRefreshCount e PresentCount atribuição de quadro apresenta.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="3ed6b-135">Se o PresentRefreshCount da última amostra não corresponder ao PresentCount (ou seja, se o PresentRefreshCount tiver sido incrementado, mas PresentCount não tiver, havia um descarte de quadros.)</span><span class="sxs-lookup"><span data-stu-id="3ed6b-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="3ed6b-136">Os aplicativos podem determinar se um quadro foi descartado por amostragem de duas instâncias de PresentCount e GetPresentStats (chamando a API GetPresentStats em dois pontos no tempo).</span><span class="sxs-lookup"><span data-stu-id="3ed6b-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="3ed6b-137">Por exemplo, um aplicativo de mídia que está apresentando na mesma taxa que a taxa de atualização do monitor (por exemplo, a taxa de atualização do monitor é de 60, o aplicativo apresenta um quadro a cada 1/60 segundos) quer apresentar os quadros A, B, C, D, E, cada um correspondendo às IDs presentes (PresentCount) 1, 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="3ed6b-138">O código do aplicativo é semelhante à sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="3ed6b-139">Renderizar o quadro a para o buffer de fundo</span><span class="sxs-lookup"><span data-stu-id="3ed6b-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="3ed6b-140">Chamada presente, PresentCount = 1</span><span class="sxs-lookup"><span data-stu-id="3ed6b-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="3ed6b-141">Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="3ed6b-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="3ed6b-142">Renderizar os próximos 4 quadros, B, C, D, E, respectivamente</span><span class="sxs-lookup"><span data-stu-id="3ed6b-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="3ed6b-143">Chamada presente 4 vezes, PresentCounts = 2, 3, 7, 8, respectivamente</span><span class="sxs-lookup"><span data-stu-id="3ed6b-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="3ed6b-144">Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="3ed6b-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="3ed6b-145">Compare os valores de PresentRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="3ed6b-146">Se a diferença for 2, ou seja, 2 intervalos de vblank decorridos entre as duas chamadas de API GetPresentStats, o último quadro apresentado deverá ser o quadro C. Como o aplicativo apresenta uma vez vblank intervalo (a taxa de atualização do monitor), o tempo decorrido entre quando o quadro A é apresentado e quando o quadro C é apresentado deve ser 2 vblanks.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="3ed6b-147">Compare os valores de PresentCount das duas estruturas D3DPRESENTSTATS armazenadas.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="3ed6b-148">Se o primeiro PresentCount for 1 (correspondente ao quadro A) e o segundo PresentCount for 3 (correspondente ao quadro C), nenhum quadro foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="3ed6b-149">Se o segundo PresentCount for 3, que corresponde ao quadro D, o aplicativo saberá que um quadro foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="3ed6b-150">Observe que GetPresentStatistics será processado depois que for chamado, independentemente do estado de chamadas PresentEx do modo FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="3ed6b-151">**Windows Vista:** As chamadas presentes serão enfileiradas e, em seguida, processadas antes que a chamada a GetPresentStats seja processada.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="3ed6b-152">Quando um aplicativo detecta que a apresentação de determinados quadros está atrás, ele pode ignorar esses quadros e corrigir a apresentação para sincronizar novamente com o vblank.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="3ed6b-153">Para fazer isso, um aplicativo pode simplesmente não renderizar os quadros atrasados e iniciar a renderização com o próximo quadro correto na fila.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="3ed6b-154">No entanto, se um aplicativo já tiver iniciado o processamento de quadros atrasados, ele poderá usar um novo parâmetro presente em D3D9Ex chamado D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="3ed6b-155">O sinalizador será passado nos parâmetros da chamada de API atual e indicará o tempo de execução que o quadro será processado imediatamente no próximo intervalo de vblank, efetivamente não visível na tela.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="3ed6b-156">Aqui está o exemplo de uso do aplicativo após a última etapa no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="3ed6b-157">Renderizar o próximo quadro para o buffer de fundo</span><span class="sxs-lookup"><span data-stu-id="3ed6b-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="3ed6b-158">Descobrir de PresentRefreshCount que o próximo quadro já está atrasado</span><span class="sxs-lookup"><span data-stu-id="3ed6b-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="3ed6b-159">Definir intervalo atual para D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="3ed6b-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="3ed6b-160">Chamada presente no próximo quadro</span><span class="sxs-lookup"><span data-stu-id="3ed6b-160">Call Present on the next frame</span></span>

<span data-ttu-id="3ed6b-161">Os aplicativos podem sincronizar fluxos de áudio e vídeo da mesma maneira porque o comportamento de GetPresentStatistics não é alterado nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="3ed6b-162">O modo flip D3D9Ex fornece informações de estatísticas de quadro para aplicativos em janelas e aplicativos de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="3ed6b-163">**Windows Vista:** Use as APIs do DWM para recuperar as estatísticas presentes.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="3ed6b-164">Quando Gerenciador de Janelas da Área de Trabalho estiver desativada, o modo em janela do 9Ex Applications usando o modo flip receberá informações estatísticas atuais de precisão limitada.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="3ed6b-165">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="3ed6b-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="3ed6b-166">Se um aplicativo não for rápido o suficiente para acompanhar a taxa de atualização do monitor, possivelmente devido ao hardware lento ou à falta de recursos do sistema, ele poderá enfrentar uma falha de gráficos.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="3ed6b-167">Uma falha é uma chamada intermitência Visual.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="3ed6b-168">Se um monitor estiver configurado para ser atualizado em 60 Hz, e o aplicativo só puder gerenciar 30 fps, metade dos quadros terá problemas.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="3ed6b-169">Os aplicativos podem detectar uma falha mantendo o controle do SynchRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="3ed6b-170">Por exemplo, um aplicativo pode executar a seguinte sequência de ações.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="3ed6b-171">Renderizar para o buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="3ed6b-172">Chamada presente.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-172">Call Present.</span></span>
3.  <span data-ttu-id="3ed6b-173">Chame GetPresentStats e armazene a estrutura D3DPRESENTSTATS resultante.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="3ed6b-174">Renderizar o próximo quadro para o buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="3ed6b-175">Chamada presente.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-175">Call Present.</span></span>
6.  <span data-ttu-id="3ed6b-176">Chame GetPresentStats e armazene a estrutura D3DPRESENTSTATS resultante.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="3ed6b-177">Compare os valores de SyncRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="3ed6b-178">Se a diferença for maior que um, um quadro foi ignorado.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed6b-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed6b-179">Requirements</span></span>



| <span data-ttu-id="3ed6b-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed6b-180">Requirement</span></span> | <span data-ttu-id="3ed6b-181">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed6b-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed6b-182">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ed6b-182">Header</span></span><br/> | <dl> <span data-ttu-id="3ed6b-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed6b-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed6b-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed6b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed6b-185">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="3ed6b-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
