---
title: Solucionando problemas de aplicativos
description: Esta seção fornece soluções para problemas comuns.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch, solução de problemas de aplicativos
- Windows Touch, rejeição de Palm
- rejeição do Palm
- Windows Touch, suporte herdado
- solução de problemas do Windows Touch
- inércia, solução de problemas de aplicativos
- manipulações, solução de problemas de aplicativos
- gestos, aplicativos de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443137"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="28903-111">Solucionando problemas de aplicativos</span><span class="sxs-lookup"><span data-stu-id="28903-111">Troubleshooting Applications</span></span>

<span data-ttu-id="28903-112">Esta seção fornece soluções para problemas comuns.</span><span class="sxs-lookup"><span data-stu-id="28903-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="28903-113">Solução de problemas gerais</span><span class="sxs-lookup"><span data-stu-id="28903-113">General Troubleshooting</span></span>



| <span data-ttu-id="28903-114">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-114">Category</span></span> | <span data-ttu-id="28903-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-116">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-116">Issue</span></span>    | <span data-ttu-id="28903-117">Estou executando o Windows Server 2008 e os recursos do Windows Touch não estão funcionando.</span><span class="sxs-lookup"><span data-stu-id="28903-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="28903-118">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-118">Cause</span></span>    | <span data-ttu-id="28903-119">Você não habilitou a experiência desktop.</span><span class="sxs-lookup"><span data-stu-id="28903-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="28903-120">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-120">Solution</span></span> | <span data-ttu-id="28903-121">Abra a ferramenta administrativa do Gerenciador do Servidor: clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciador do servidor**.</span><span class="sxs-lookup"><span data-stu-id="28903-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="28903-122">Clique no item **recursos** na coluna esquerda.</span><span class="sxs-lookup"><span data-stu-id="28903-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="28903-123">Clique em **Adicionar recursos** na seção **recursos** .</span><span class="sxs-lookup"><span data-stu-id="28903-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="28903-124">Selecione **experiência da área de trabalho**, clique em **Avançar** e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="28903-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="28903-125">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-125">Category</span></span> | <span data-ttu-id="28903-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-127">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-127">Issue</span></span>    | <span data-ttu-id="28903-128">Sempre que eu mover meu dedo rapidamente pelo meu aplicativo, uma seta é exibida e meu gesto ou manipulação não está registrando corretamente.</span><span class="sxs-lookup"><span data-stu-id="28903-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="28903-129">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-129">Cause</span></span>    | <span data-ttu-id="28903-130">Ter movimentos habilitados quando você não precisa dele.</span><span class="sxs-lookup"><span data-stu-id="28903-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="28903-131">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-131">Solution</span></span> | <span data-ttu-id="28903-132">Você tem movimentos habilitados quando deseja que ele seja desabilitado.</span><span class="sxs-lookup"><span data-stu-id="28903-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="28903-133">Consulte [suporte herdado para panorâmica com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) para obter informações sobre como desabilitar movimentos de caneta.</span><span class="sxs-lookup"><span data-stu-id="28903-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28903-134">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-134">Issue</span></span></td>
<td><span data-ttu-id="28903-135">Não consigo distinguir entre entrada do mouse e entrada do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="28903-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28903-136">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-136">Cause</span></span></td>
<td><span data-ttu-id="28903-137">O Windows gera mensagens de mouse para suporte herdado quando um usuário clica na tela.</span><span class="sxs-lookup"><span data-stu-id="28903-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28903-138">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-138">Solution</span></span></td>
<td><span data-ttu-id="28903-139">Você pode chamar <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> para o <strong>WM_LBUTTONDOWN</strong> e <strong>WM_LBUTTONUP</strong> mensagens para determinar a origem.</span><span class="sxs-lookup"><span data-stu-id="28903-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="28903-140">O código a seguir mostra como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="28903-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28903-141">C++</span><span class="sxs-lookup"><span data-stu-id="28903-141">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="28903-142">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-142">Category</span></span> | <span data-ttu-id="28903-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-144">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-144">Issue</span></span>    | <span data-ttu-id="28903-145">Como fazer executar aplicativos do Microsoft PixelSense no Windows 7?</span><span class="sxs-lookup"><span data-stu-id="28903-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="28903-146">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-146">Cause</span></span>    | <span data-ttu-id="28903-147">O Windows Touch e o Microsoft PixelSense são incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="28903-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="28903-148">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-148">Solution</span></span> | <span data-ttu-id="28903-149">Você precisa direcionar para a plataforma Windows 7 ou para a plataforma Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="28903-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="28903-150">Solucionando problemas de manipulação e inércia</span><span class="sxs-lookup"><span data-stu-id="28903-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="28903-151">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-151">Category</span></span> | <span data-ttu-id="28903-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-153">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-153">Issue</span></span>    | <span data-ttu-id="28903-154">Meu aplicativo está congelando sem motivo.</span><span class="sxs-lookup"><span data-stu-id="28903-154">My application is freezing for no reason.</span></span> <span data-ttu-id="28903-155">Estou obtendo violações de acesso quando inicializo as interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="28903-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="28903-156">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-156">Cause</span></span>    | <span data-ttu-id="28903-157">Falta uma chamada para o **CoInitialize** ao usar as interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) ou [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="28903-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="28903-158">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-158">Solution</span></span> | <span data-ttu-id="28903-159">Isso pode ser causado pela instanciação dos objetos COM (Windows Touch Component Object Model) sem chamar o CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="28903-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="28903-160">Isso ocorre às vezes, quando você está convertendo projetos do uso de gestos para usar as interfaces Manipulation ou inércia.</span><span class="sxs-lookup"><span data-stu-id="28903-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="28903-161">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-161">Category</span></span> | <span data-ttu-id="28903-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-163">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-163">Issue</span></span>    | <span data-ttu-id="28903-164">Meu objeto está girando de forma inadequada quando está sendo traduzido.</span><span class="sxs-lookup"><span data-stu-id="28903-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="28903-165">A rotação de um único dedo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="28903-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="28903-166">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-166">Cause</span></span>    | <span data-ttu-id="28903-167">Configuração inadequada de pivôs em um objeto.</span><span class="sxs-lookup"><span data-stu-id="28903-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="28903-168">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-168">Solution</span></span> | <span data-ttu-id="28903-169">Você não está configurando os pontos de manipulação dinâmica corretamente.</span><span class="sxs-lookup"><span data-stu-id="28903-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="28903-170">Defina as propriedades [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) e [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) como o centro do objeto ou o ponto que você deseja girar e defina a propriedade [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) como o raio do seu objeto.</span><span class="sxs-lookup"><span data-stu-id="28903-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="28903-171">Solucionando problemas de entrada por toque do Windows</span><span class="sxs-lookup"><span data-stu-id="28903-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="28903-172">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-172">Category</span></span> | <span data-ttu-id="28903-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-174">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-174">Issue</span></span>    | <span data-ttu-id="28903-175">Depois de lidar com a mensagem do [**WM \_ Touch**](wm-touchdown.md) , eu pare de obter comentários sobre limites.</span><span class="sxs-lookup"><span data-stu-id="28903-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="28903-176">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-176">Cause</span></span>    | <span data-ttu-id="28903-177">Consumindo a mensagem do [**WM \_ Touch**](wm-touchdown.md) sem tratá-la.</span><span class="sxs-lookup"><span data-stu-id="28903-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="28903-178">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-178">Solution</span></span> | <span data-ttu-id="28903-179">Provavelmente, você está consumindo uma mensagem do Windows Touch sem encaminhá-la para **DefWindowProc**, o que resultará em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="28903-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="28903-180">Verifique [introdução com as mensagens do Windows Touch](getting-started-with-multi-touch-messages.md) para obter mais informações sobre como lidar corretamente com o [**WM \_ Touch**](wm-touchdown.md) messages.</span><span class="sxs-lookup"><span data-stu-id="28903-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28903-181">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-181">Issue</span></span></td>
<td><span data-ttu-id="28903-182">Estou incluindo o Windows. h, mas ainda diz que <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> não está definido.</span><span class="sxs-lookup"><span data-stu-id="28903-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28903-183">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-183">Cause</span></span></td>
<td><span data-ttu-id="28903-184">A versão do Windows em targetver. h está incorreta.</span><span class="sxs-lookup"><span data-stu-id="28903-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28903-185">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-185">Solution</span></span></td>
<td><span data-ttu-id="28903-186">Você não definiu a versão correta do Windows no seu projeto.</span><span class="sxs-lookup"><span data-stu-id="28903-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="28903-187">O código a seguir ilustra as versões do Windows definidas corretamente para o Windows Touch no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28903-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28903-188">C++</span><span class="sxs-lookup"><span data-stu-id="28903-188">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28903-189">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-189">Issue</span></span></td>
<td><span data-ttu-id="28903-190">Minhas coordenadas x de entrada por toque e coordenadas y parecem inválidas.</span><span class="sxs-lookup"><span data-stu-id="28903-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="28903-191">Eles são valores maiores que o esperado ou são valores negativos.</span><span class="sxs-lookup"><span data-stu-id="28903-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28903-192">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-192">Cause</span></span></td>
<td><span data-ttu-id="28903-193">Talvez seja necessário converter seus pontos de toque em pixels, ou talvez seja necessário converter as coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="28903-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28903-194">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-194">Solution</span></span></td>
<td><span data-ttu-id="28903-195">Certifique-se de que você está chamando <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> e <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="28903-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="28903-196">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="28903-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28903-197">C++</span><span class="sxs-lookup"><span data-stu-id="28903-197">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="28903-198">Para usar a função <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> , você deve ter suporte a DPI alto em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28903-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="28903-199">Para obter mais informações sobre como dar suporte a DPI alto, visite a seção <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">alta dpi</a> do MSDN.</span><span class="sxs-lookup"><span data-stu-id="28903-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="28903-200">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-200">Category</span></span> | <span data-ttu-id="28903-201">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-202">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-202">Issue</span></span>    | <span data-ttu-id="28903-203">Não estou vendo mensagens [**WM \_ TOUCH,**](wm-touchdown.md) mas sei que Windows Touch está funcionando porque estou vendo mensagens [**WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="28903-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="28903-204">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-204">Cause</span></span>    | <span data-ttu-id="28903-205">Falta uma chamada para [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="28903-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="28903-206">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-206">Solution</span></span> | <span data-ttu-id="28903-207">[**WM \_ As mensagens TOUCH**](wm-touchdown.md) [**e WM \_ GESTURE**](wm-gesture.md) são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="28903-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="28903-208">Se você não chamar [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)receberá apenas mensagens **WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="28903-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="28903-209">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-209">Category</span></span> | <span data-ttu-id="28903-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-211">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-211">Issue</span></span>    | <span data-ttu-id="28903-212">Estou observando pequenos atrasos desde o momento em que toco meu dedo para baixo até quando estou recebendo entrada em meu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28903-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="28903-213">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-213">Cause</span></span>    | <span data-ttu-id="28903-214">A rejeição de mão está causando atrasos na entrada.</span><span class="sxs-lookup"><span data-stu-id="28903-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="28903-215">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-215">Solution</span></span> | <span data-ttu-id="28903-216">Se **tWF \_ WANTPALM for definido** em chamadas para [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)a rejeição de mão será habilitada.</span><span class="sxs-lookup"><span data-stu-id="28903-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="28903-217">Isso causa um pequeno atraso (100 ms) enquanto o software testa se a entrada é proveniente de um dedo, caneta ou da mão do usuário.</span><span class="sxs-lookup"><span data-stu-id="28903-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="28903-218">Desabilite a rejeição de mão **chamando RegisterTouchWindow** com o **sinalizador \_ TWF WANTPALM** limpo.</span><span class="sxs-lookup"><span data-stu-id="28903-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="28903-219">Solução de problemas Windows Touch gestos</span><span class="sxs-lookup"><span data-stu-id="28903-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="28903-220">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-220">Category</span></span> | <span data-ttu-id="28903-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-222">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-222">Issue</span></span>    | <span data-ttu-id="28903-223">Depois de lidar com [**a mensagem WM \_ GESTURE,**](wm-gesture.md) eu para de receber comentários de limite.</span><span class="sxs-lookup"><span data-stu-id="28903-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="28903-224">Ou então, um gesto que funcionou anteriormente não funciona agora.</span><span class="sxs-lookup"><span data-stu-id="28903-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="28903-225">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-225">Cause</span></span>    | <span data-ttu-id="28903-226">Consumindo a [**mensagem WM \_ GESTURE**](wm-gesture.md) sem lidar com ela.</span><span class="sxs-lookup"><span data-stu-id="28903-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="28903-227">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-227">Solution</span></span> | <span data-ttu-id="28903-228">Você provavelmente está consumindo uma Windows Touch sem encaminhá-la para [DefWindowProc,](/windows/win32/api/winuser/nf-winuser-defwindowproca)o que resultará em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="28903-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="28903-229">Verifique [Ponto de Partida com gestos do Windows](getting-started-with-multi-touch-gestures.md) para obter mais informações sobre como lidar corretamente com mensagens WM [**\_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="28903-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="28903-230">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-230">Category</span></span> | <span data-ttu-id="28903-231">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-232">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-232">Issue</span></span>    | <span data-ttu-id="28903-233">Não estou vendo mensagens [**WM \_ GESTURE,**](wm-gesture.md) mas sei que Windows Touch está funcionando porque estou vendo mensagens [**WM \_ TOUCH.**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="28903-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="28903-234">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-234">Cause</span></span>    | <span data-ttu-id="28903-235">Chamando [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="28903-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="28903-236">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-236">Solution</span></span> | <span data-ttu-id="28903-237">[**WM \_ As mensagens TOUCH**](wm-touchdown.md) [**e WM \_ GESTURE**](wm-gesture.md) são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="28903-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="28903-238">Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), não receberá mensagens **WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="28903-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28903-239">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-239">Issue</span></span></td>
<td><span data-ttu-id="28903-240">Não estou vendo todos os gestos que espero ver.</span><span class="sxs-lookup"><span data-stu-id="28903-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="28903-241">Por exemplo, estou vendo gestos com o identificador <strong>GID_PAN</strong> mas não <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="28903-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28903-242">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-242">Cause</span></span></td>
<td><span data-ttu-id="28903-243">Alguns gestos, como o gesto de rotação, não são habilitados por padrão.</span><span class="sxs-lookup"><span data-stu-id="28903-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28903-244">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-244">Solution</span></span></td>
<td><span data-ttu-id="28903-245">Você precisa chamar <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> quando receber uma mensagem <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> conforme descrito na referência <strong>do WM_GESTURENOTIFY</strong> ou você precisa adicionar um manipulador para a mensagem <strong>WM_GESTURENOTIFY.</strong></span><span class="sxs-lookup"><span data-stu-id="28903-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="28903-246">O código a seguir mostra como um manipulador pode ser implementado para habilitar o suporte para rotação.</span><span class="sxs-lookup"><span data-stu-id="28903-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28903-247">C++</span><span class="sxs-lookup"><span data-stu-id="28903-247">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="28903-248">Para obter mais exemplos de configurações de gestos típicas, <strong>consulte SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="28903-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="28903-249">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-249">Category</span></span> | <span data-ttu-id="28903-250">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-251">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-251">Issue</span></span>    | <span data-ttu-id="28903-252">As barras de rolagem personalizadas em meu aplicativo não estão rolando quando eu executar o gesto de panor rolante.</span><span class="sxs-lookup"><span data-stu-id="28903-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="28903-253">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-253">Cause</span></span>    | <span data-ttu-id="28903-254">Manipuladores ausentes para as mensagens WM \_ \* SCROLL corretas.</span><span class="sxs-lookup"><span data-stu-id="28903-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="28903-255">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-255">Solution</span></span> | <span data-ttu-id="28903-256">Você não está tratando todas as mensagens WM \_ \* SCROLL em suas barras de rolagem personalizadas.</span><span class="sxs-lookup"><span data-stu-id="28903-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="28903-257">É recomendável manipular a mensagem [**WM \_ GESTURE**](wm-gesture.md) em vez de manter a funcionalidade da barra de rolagem personalizada por meio do suporte herdado.</span><span class="sxs-lookup"><span data-stu-id="28903-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="28903-258">Você precisa dar suporte a mensagens conforme detalhado na seção Suporte herdado para panorâmico [com barras de rolagem](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="28903-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="28903-259">Categoria</span><span class="sxs-lookup"><span data-stu-id="28903-259">Category</span></span> | <span data-ttu-id="28903-260">Descrição</span><span class="sxs-lookup"><span data-stu-id="28903-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28903-261">Problema</span><span class="sxs-lookup"><span data-stu-id="28903-261">Issue</span></span>    | <span data-ttu-id="28903-262">Estou recebendo atrasos para gestos.</span><span class="sxs-lookup"><span data-stu-id="28903-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="28903-263">Causa</span><span class="sxs-lookup"><span data-stu-id="28903-263">Cause</span></span>    | <span data-ttu-id="28903-264">Os movimento podem estar causando atrasos para gestos.</span><span class="sxs-lookup"><span data-stu-id="28903-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="28903-265">Solução</span><span class="sxs-lookup"><span data-stu-id="28903-265">Solution</span></span> | <span data-ttu-id="28903-266">Os movimento podem causar atrasos quanto tempo leva para o aplicativo receber [**mensagens WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="28903-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="28903-267">Consulte [Suporte herdado para panorâmico com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) para obter informações sobre como desabilitar movimento.</span><span class="sxs-lookup"><span data-stu-id="28903-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="28903-268">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28903-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28903-269">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="28903-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 