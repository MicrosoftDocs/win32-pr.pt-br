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
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930266"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="9b8cd-111">Solucionando problemas de aplicativos</span><span class="sxs-lookup"><span data-stu-id="9b8cd-111">Troubleshooting Applications</span></span>

<span data-ttu-id="9b8cd-112">Esta seção fornece soluções para problemas comuns.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="9b8cd-113">Solução de problemas gerais</span><span class="sxs-lookup"><span data-stu-id="9b8cd-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-114">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-114">Issue</span></span>    | <span data-ttu-id="9b8cd-115">Estou executando o Windows Server 2008 e os recursos do Windows Touch não estão funcionando.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="9b8cd-116">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-116">Cause</span></span>    | <span data-ttu-id="9b8cd-117">Você não habilitou a experiência desktop.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b8cd-118">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-118">Solution</span></span> | <span data-ttu-id="9b8cd-119">Abra a ferramenta administrativa do Gerenciador do Servidor: clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciador do servidor**.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="9b8cd-120">Clique no item **recursos** na coluna esquerda.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="9b8cd-121">Clique em **Adicionar recursos** na seção **recursos** .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="9b8cd-122">Selecione **experiência da área de trabalho**, clique em **Avançar** e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-123">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-123">Issue</span></span>    | <span data-ttu-id="9b8cd-124">Sempre que eu mover meu dedo rapidamente pelo meu aplicativo, uma seta é exibida e meu gesto ou manipulação não está registrando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="9b8cd-125">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-125">Cause</span></span>    | <span data-ttu-id="9b8cd-126">Ter movimentos habilitados quando você não precisa dele.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9b8cd-127">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-127">Solution</span></span> | <span data-ttu-id="9b8cd-128">Você tem movimentos habilitados quando deseja que ele seja desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="9b8cd-129">Consulte [suporte herdado para panorâmica com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) para obter informações sobre como desabilitar movimentos de caneta.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b8cd-130">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-130">Issue</span></span></td>
<td><span data-ttu-id="9b8cd-131">Não consigo distinguir entre entrada do mouse e entrada do Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8cd-132">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-132">Cause</span></span></td>
<td><span data-ttu-id="9b8cd-133">O Windows gera mensagens de mouse para suporte herdado quando um usuário clica na tela.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b8cd-134">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-134">Solution</span></span></td>
<td><span data-ttu-id="9b8cd-135">Você pode chamar <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> para o <strong>WM_LBUTTONDOWN</strong> e <strong>WM_LBUTTONUP</strong> mensagens para determinar a origem.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="9b8cd-136">O código a seguir mostra como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b8cd-137">C++</span><span class="sxs-lookup"><span data-stu-id="9b8cd-137">C++</span></span></th>
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



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-138">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-138">Issue</span></span>    | <span data-ttu-id="9b8cd-139">Como fazer executar aplicativos do Microsoft PixelSense no Windows 7?</span><span class="sxs-lookup"><span data-stu-id="9b8cd-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="9b8cd-140">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-140">Cause</span></span>    | <span data-ttu-id="9b8cd-141">O Windows Touch e o Microsoft PixelSense são incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="9b8cd-142">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-142">Solution</span></span> | <span data-ttu-id="9b8cd-143">Você precisa direcionar para a plataforma Windows 7 ou para a plataforma Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="9b8cd-144">Solucionando problemas de manipulação e inércia</span><span class="sxs-lookup"><span data-stu-id="9b8cd-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-145">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-145">Issue</span></span>    | <span data-ttu-id="9b8cd-146">Meu aplicativo está congelando sem motivo.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-146">My application is freezing for no reason.</span></span> <span data-ttu-id="9b8cd-147">Estou obtendo violações de acesso quando inicializo as interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="9b8cd-148">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-148">Cause</span></span>    | <span data-ttu-id="9b8cd-149">Falta uma chamada para o **CoInitialize** ao usar as interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) ou [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="9b8cd-150">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-150">Solution</span></span> | <span data-ttu-id="9b8cd-151">Isso pode ser causado pela instanciação dos objetos COM (Windows Touch Component Object Model) sem chamar o CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="9b8cd-152">Isso ocorre às vezes, quando você está convertendo projetos do uso de gestos para usar as interfaces Manipulation ou inércia.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-153">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-153">Issue</span></span>    | <span data-ttu-id="9b8cd-154">Meu objeto está girando de forma inadequada quando está sendo traduzido.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="9b8cd-155">A rotação de um único dedo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b8cd-156">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-156">Cause</span></span>    | <span data-ttu-id="9b8cd-157">Configuração inadequada de pivôs em um objeto.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b8cd-158">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-158">Solution</span></span> | <span data-ttu-id="9b8cd-159">Você não está configurando os pontos de manipulação dinâmica corretamente.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="9b8cd-160">Defina as propriedades [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) e [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) como o centro do objeto ou o ponto que você deseja girar e defina a propriedade [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) como o raio do seu objeto.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="9b8cd-161">Solucionando problemas de entrada por toque do Windows</span><span class="sxs-lookup"><span data-stu-id="9b8cd-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-162">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-162">Issue</span></span>    | <span data-ttu-id="9b8cd-163">Depois de lidar com a mensagem do [**WM \_ Touch**](wm-touchdown.md) , eu pare de obter comentários sobre limites.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="9b8cd-164">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-164">Cause</span></span>    | <span data-ttu-id="9b8cd-165">Consumindo a mensagem do [**WM \_ Touch**](wm-touchdown.md) sem tratá-la.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b8cd-166">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-166">Solution</span></span> | <span data-ttu-id="9b8cd-167">Provavelmente, você está consumindo uma mensagem do Windows Touch sem encaminhá-la para **DefWindowProc**, o que resultará em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="9b8cd-168">Verifique [introdução com as mensagens do Windows Touch](getting-started-with-multi-touch-messages.md) para obter mais informações sobre como lidar corretamente com o [**WM \_ Touch**](wm-touchdown.md) messages.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b8cd-169">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-169">Issue</span></span></td>
<td><span data-ttu-id="9b8cd-170">Estou incluindo o Windows. h, mas ainda diz que <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> não está definido.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8cd-171">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-171">Cause</span></span></td>
<td><span data-ttu-id="9b8cd-172">A versão do Windows em targetver. h está incorreta.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b8cd-173">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-173">Solution</span></span></td>
<td><span data-ttu-id="9b8cd-174">Você não definiu a versão correta do Windows no seu projeto.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="9b8cd-175">O código a seguir ilustra as versões do Windows definidas corretamente para o Windows Touch no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b8cd-176">C++</span><span class="sxs-lookup"><span data-stu-id="9b8cd-176">C++</span></span></th>
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
<td><span data-ttu-id="9b8cd-177">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-177">Issue</span></span></td>
<td><span data-ttu-id="9b8cd-178">Minhas coordenadas x de entrada por toque e coordenadas y parecem inválidas.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="9b8cd-179">Eles são valores maiores que o esperado ou são valores negativos.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8cd-180">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-180">Cause</span></span></td>
<td><span data-ttu-id="9b8cd-181">Talvez seja necessário converter seus pontos de toque em pixels, ou talvez seja necessário converter as coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b8cd-182">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-182">Solution</span></span></td>
<td><span data-ttu-id="9b8cd-183">Certifique-se de que você está chamando <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> e <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="9b8cd-184">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b8cd-185">C++</span><span class="sxs-lookup"><span data-stu-id="9b8cd-185">C++</span></span></th>
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
<span data-ttu-id="9b8cd-186">Para usar a função <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> , você deve ter suporte a DPI alto em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="9b8cd-187">Para obter mais informações sobre como dar suporte a DPI alto, visite a seção <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">alta dpi</a> do MSDN.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-188">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-188">Issue</span></span>    | <span data-ttu-id="9b8cd-189">Não estou vendo as mensagens do [**WM \_ Touch**](wm-touchdown.md) , mas sei que o Windows Touch está funcionando porque estou vendo as mensagens de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="9b8cd-190">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-190">Cause</span></span>    | <span data-ttu-id="9b8cd-191">Uma chamada para [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)está ausente.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="9b8cd-192">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-192">Solution</span></span> | <span data-ttu-id="9b8cd-193">[**WM \_**](wm-touchdown.md) As mensagens [**de \_ gesto**](wm-gesture.md) do touch e do WM são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="9b8cd-194">Se você não chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), receberá apenas mensagens **de \_ gesto do WM** .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-195">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-195">Issue</span></span>    | <span data-ttu-id="9b8cd-196">Estou percebendo pequenos atrasos no momento em que eu toque meu dedo quando estou recebendo entrada no meu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="9b8cd-197">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-197">Cause</span></span>    | <span data-ttu-id="9b8cd-198">A rejeição do Palm está causando atrasos na entrada.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9b8cd-199">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-199">Solution</span></span> | <span data-ttu-id="9b8cd-200">Se **TWF \_ WANTPALM** for definido em chamadas para [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), a rejeição de Palm estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="9b8cd-201">Isso causa um pequeno atraso de (100 ms) enquanto o software testa se a entrada é proveniente de um dedo, caneta ou da palma do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="9b8cd-202">Desabilite a rejeição de Palm chamando **RegisterTouchWindow** com o sinalizador **TWF \_ WANTPALM** limpo.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="9b8cd-203">Solução de problemas de gestos de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="9b8cd-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-204">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-204">Issue</span></span>    | <span data-ttu-id="9b8cd-205">Depois de manipular a mensagem de [**\_ gesto do WM**](wm-gesture.md) , pare de obter comentários sobre limites.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="9b8cd-206">Ou então, um gesto que funcionou anteriormente não funciona agora.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="9b8cd-207">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-207">Cause</span></span>    | <span data-ttu-id="9b8cd-208">Consumindo a mensagem de [**\_ gesto do WM**](wm-gesture.md) sem tratá-la.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9b8cd-209">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-209">Solution</span></span> | <span data-ttu-id="9b8cd-210">Provavelmente, você está consumindo uma mensagem do Windows Touch sem encaminhá-la para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), o que resultará em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="9b8cd-211">Verifique [introdução com gestos do Windows](getting-started-with-multi-touch-gestures.md) para obter mais informações sobre como lidar corretamente com as mensagens de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-212">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-212">Issue</span></span>    | <span data-ttu-id="9b8cd-213">Não estou vendo as mensagens de [**\_ gestos do WM**](wm-gesture.md) , mas sei que o Windows Touch está funcionando porque estou vendo as mensagens do [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="9b8cd-214">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-214">Cause</span></span>    | <span data-ttu-id="9b8cd-215">Chamando [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="9b8cd-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="9b8cd-216">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-216">Solution</span></span> | <span data-ttu-id="9b8cd-217">[**WM \_**](wm-touchdown.md) As mensagens [**de \_ gesto**](wm-gesture.md) do touch e do WM são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="9b8cd-218">Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), não receberá mensagens **de \_ gesto do WM** .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b8cd-219">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-219">Issue</span></span></td>
<td><span data-ttu-id="9b8cd-220">Não estou vendo todos os gestos que espero ver.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="9b8cd-221">Por exemplo, estou vendo gestos com o identificador <strong>GID_PAN</strong> mas não <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b8cd-222">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-222">Cause</span></span></td>
<td><span data-ttu-id="9b8cd-223">Alguns gestos, como o gesto de rotação, não são habilitados por padrão.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b8cd-224">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-224">Solution</span></span></td>
<td><span data-ttu-id="9b8cd-225">Você precisa chamar <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> quando receber uma mensagem de <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> conforme descrito na referência de <strong>WM_GESTURENOTIFY</strong> ou precisar adicionar um manipulador para a mensagem de <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="9b8cd-226">O código a seguir mostra como um manipulador pode ser implementado para habilitar o suporte para rotação.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b8cd-227">C++</span><span class="sxs-lookup"><span data-stu-id="9b8cd-227">C++</span></span></th>
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

<span data-ttu-id="9b8cd-228">Para obter mais exemplos de configurações de gesto típicas, consulte <strong>SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-229">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-229">Issue</span></span>    | <span data-ttu-id="9b8cd-230">As barras de rolagem personalizadas no meu aplicativo não estão rolando quando executo o gesto de panorâmica.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9b8cd-231">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-231">Cause</span></span>    | <span data-ttu-id="9b8cd-232">Manipuladores ausentes para as \_ mensagens de rolagem corretas do WM \* .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9b8cd-233">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-233">Solution</span></span> | <span data-ttu-id="9b8cd-234">Você não está lidando com todas as \_ \* mensagens de rolagem do WM em suas barras de rolagem personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="9b8cd-235">É recomendável que você manipule a mensagem de [**\_ gesto do WM**](wm-gesture.md) em vez de manter a funcionalidade de barra de rolagem personalizada por meio do suporte herdado.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="9b8cd-236">Você precisa dar suporte a mensagens, conforme detalhado na seção [suporte herdado para movimento panorâmico com barras de rolagem](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cd-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cd-237">Problema</span><span class="sxs-lookup"><span data-stu-id="9b8cd-237">Issue</span></span>    | <span data-ttu-id="9b8cd-238">Estou recebendo atrasos para gestos.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9b8cd-239">Causa</span><span class="sxs-lookup"><span data-stu-id="9b8cd-239">Cause</span></span>    | <span data-ttu-id="9b8cd-240">Os movimentos podem estar causando atrasos para gestos.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="9b8cd-241">Solução</span><span class="sxs-lookup"><span data-stu-id="9b8cd-241">Solution</span></span> | <span data-ttu-id="9b8cd-242">Os movimentos podem causar atrasos por quanto tempo leva para seu aplicativo receber mensagens [**de \_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="9b8cd-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="9b8cd-243">Consulte [suporte herdado para panorâmica com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) para obter informações sobre como desabilitar movimentos.</span><span class="sxs-lookup"><span data-stu-id="9b8cd-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9b8cd-244">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b8cd-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b8cd-245">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="9b8cd-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 