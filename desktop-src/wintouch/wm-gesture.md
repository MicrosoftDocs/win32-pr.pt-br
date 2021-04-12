---
title: Mensagem de WM_GESTURE (WinUser. h)
description: Passa informações sobre um gesto.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE a mensagem Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369756"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="e3cad-104">Mensagem de gesto do WM \_</span><span class="sxs-lookup"><span data-stu-id="e3cad-104">WM\_GESTURE message</span></span>

<span data-ttu-id="e3cad-105">Passa informações sobre um gesto.</span><span class="sxs-lookup"><span data-stu-id="e3cad-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3cad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3cad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3cad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cad-108">Fornece informações que identificam o comando de gesto e os valores de argumento específicos do gesto.</span><span class="sxs-lookup"><span data-stu-id="e3cad-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="e3cad-109">Essas informações são as mesmas informações passadas para o membro **ullArguments** da estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3cad-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3cad-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3cad-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cad-111">Fornece um identificador para informações que identificam o comando de gesto e os valores de argumento específicos do gesto.</span><span class="sxs-lookup"><span data-stu-id="e3cad-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="e3cad-112">Essas informações são recuperadas chamando [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span><span class="sxs-lookup"><span data-stu-id="e3cad-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3cad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3cad-113">Return value</span></span>

<span data-ttu-id="e3cad-114">Se um aplicativo processar essa mensagem, ele deverá retornar 0.</span><span class="sxs-lookup"><span data-stu-id="e3cad-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="e3cad-115">Se o aplicativo não processar a mensagem, ele deverá chamar [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e3cad-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="e3cad-116">Não fazer isso fará com que o aplicativo vazasse memória porque o identificador de entrada por toque não será fechado e a memória do processo associada não será liberada.</span><span class="sxs-lookup"><span data-stu-id="e3cad-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3cad-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3cad-117">Remarks</span></span>

<span data-ttu-id="e3cad-118">A tabela a seguir lista os comandos de gesto com suporte.</span><span class="sxs-lookup"><span data-stu-id="e3cad-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="e3cad-119">ID do gesto</span><span class="sxs-lookup"><span data-stu-id="e3cad-119">Gesture ID</span></span>            | <span data-ttu-id="e3cad-120">Valor (*dwID*)</span><span class="sxs-lookup"><span data-stu-id="e3cad-120">Value (*dwID*)</span></span> | <span data-ttu-id="e3cad-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3cad-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cad-122">**início de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="e3cad-123">1</span><span class="sxs-lookup"><span data-stu-id="e3cad-123">1</span></span>              | <span data-ttu-id="e3cad-124">Indica que um gesto genérico está começando.</span><span class="sxs-lookup"><span data-stu-id="e3cad-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="e3cad-125">**fim do GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-125">**GID\_END**</span></span>          | <span data-ttu-id="e3cad-126">2</span><span class="sxs-lookup"><span data-stu-id="e3cad-126">2</span></span>              | <span data-ttu-id="e3cad-127">Indica uma extremidade de gesto genérico.</span><span class="sxs-lookup"><span data-stu-id="e3cad-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e3cad-128">**ZOOM de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="e3cad-129">3</span><span class="sxs-lookup"><span data-stu-id="e3cad-129">3</span></span>              | <span data-ttu-id="e3cad-130">Indica início do zoom, movimentação de zoom ou parada de zoom.</span><span class="sxs-lookup"><span data-stu-id="e3cad-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="e3cad-131">A primeira mensagem de comando de **\_ zoom GID** começa um zoom, mas não causa nenhum zoom.</span><span class="sxs-lookup"><span data-stu-id="e3cad-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="e3cad-132">O segundo comando **GID de \_ zoom** dispara um zoom relativo ao estado contido no primeiro **\_ zoom GID**.</span><span class="sxs-lookup"><span data-stu-id="e3cad-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="e3cad-133">**deslocamento de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-133">**GID\_PAN**</span></span>          | <span data-ttu-id="e3cad-134">4</span><span class="sxs-lookup"><span data-stu-id="e3cad-134">4</span></span>              | <span data-ttu-id="e3cad-135">Indica a movimentação de panorâmica ou o início da panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e3cad-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="e3cad-136">O primeiro comando de **\_ Pan de GID** indica um início panorâmico, mas não executa nenhum movimento panorâmico.</span><span class="sxs-lookup"><span data-stu-id="e3cad-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="e3cad-137">Com a segunda mensagem de comando de **\_ Pan de GID** , o aplicativo começará a panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e3cad-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="e3cad-138">**rotação de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="e3cad-139">5</span><span class="sxs-lookup"><span data-stu-id="e3cad-139">5</span></span>              | <span data-ttu-id="e3cad-140">Indica o movimento de girar ou girar para começar.</span><span class="sxs-lookup"><span data-stu-id="e3cad-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="e3cad-141">A primeira mensagem de comando **GID \_ Rotate** indica uma movimentação de giro ou de giro, mas não será girada.</span><span class="sxs-lookup"><span data-stu-id="e3cad-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="e3cad-142">A segunda mensagem de comando **GID \_ Rotate** disparará uma operação de rotação relativa ao estado contido na primeira **\_ rotação de GID**.</span><span class="sxs-lookup"><span data-stu-id="e3cad-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="e3cad-143">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="e3cad-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="e3cad-144">6</span><span class="sxs-lookup"><span data-stu-id="e3cad-144">6</span></span>              | <span data-ttu-id="e3cad-145">Indica gesto de toque com dois dedos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e3cad-146">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="e3cad-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="e3cad-147">7</span><span class="sxs-lookup"><span data-stu-id="e3cad-147">7</span></span>              | <span data-ttu-id="e3cad-148">Indica o gesto de pressionar e tocar.</span><span class="sxs-lookup"><span data-stu-id="e3cad-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e3cad-149">Para habilitar o suporte herdado, as mensagens com os comandos de gesto de **\_ encerramento** de **GID \_ begin** e GID precisam ser encaminhadas usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e3cad-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="e3cad-150">A tabela a seguir indica os argumentos de gestos passados nos parâmetros *lParam* e *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e3cad-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="e3cad-151">ID do gesto</span><span class="sxs-lookup"><span data-stu-id="e3cad-151">Gesture ID</span></span>            | <span data-ttu-id="e3cad-152">Gesto</span><span class="sxs-lookup"><span data-stu-id="e3cad-152">Gesture</span></span>        | <span data-ttu-id="e3cad-153">*ullArgument*</span><span class="sxs-lookup"><span data-stu-id="e3cad-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="e3cad-154">*ptsLocation* na estrutura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)</span><span class="sxs-lookup"><span data-stu-id="e3cad-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cad-155">**ZOOM de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="e3cad-156">Ampliar/reduzir</span><span class="sxs-lookup"><span data-stu-id="e3cad-156">Zoom In/Out</span></span>    | <span data-ttu-id="e3cad-157">Indica a distância entre os dois pontos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="e3cad-158">Indica o centro do zoom.</span><span class="sxs-lookup"><span data-stu-id="e3cad-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="e3cad-159">**deslocamento de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-159">**GID\_PAN**</span></span>          | <span data-ttu-id="e3cad-160">Panorâmica</span><span class="sxs-lookup"><span data-stu-id="e3cad-160">Pan</span></span>            | <span data-ttu-id="e3cad-161">Indica a distância entre os dois pontos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="e3cad-162">Indica a posição atual da Pan.</span><span class="sxs-lookup"><span data-stu-id="e3cad-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="e3cad-163">**rotação de GID \_**</span><span class="sxs-lookup"><span data-stu-id="e3cad-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="e3cad-164">Girar (pivô)</span><span class="sxs-lookup"><span data-stu-id="e3cad-164">Rotate (pivot)</span></span> | <span data-ttu-id="e3cad-165">Indica o ângulo de rotação se o sinalizador de **\_ início GF** estiver definido.</span><span class="sxs-lookup"><span data-stu-id="e3cad-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="e3cad-166">Caso contrário, essa é a alteração de ângulo desde que a rotação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="e3cad-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="e3cad-167">Isso é assinado para indicar a direção da rotação.</span><span class="sxs-lookup"><span data-stu-id="e3cad-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="e3cad-168">Use o [**ângulo \_ \_ de giro \_ de GID de \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e o ângulo de rotação de GID para macros de [**\_ \_ \_ \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obter e definir o valor de ângulo.</span><span class="sxs-lookup"><span data-stu-id="e3cad-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="e3cad-169">Isso indica o centro da rotação que é o ponto estacionário no qual o objeto de destino é girado.</span><span class="sxs-lookup"><span data-stu-id="e3cad-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="e3cad-170">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="e3cad-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="e3cad-171">Toque com dois dedos</span><span class="sxs-lookup"><span data-stu-id="e3cad-171">Two-finger Tap</span></span> | <span data-ttu-id="e3cad-172">Indica a distância entre os dois dedos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="e3cad-173">Indica o centro dos dois dedos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="e3cad-174">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="e3cad-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="e3cad-175">Pressione e toque em</span><span class="sxs-lookup"><span data-stu-id="e3cad-175">Press and Tap</span></span>  | <span data-ttu-id="e3cad-176">Indica o Delta entre o primeiro dedo e o segundo dedo.</span><span class="sxs-lookup"><span data-stu-id="e3cad-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="e3cad-177">Esse valor é armazenado nos menores 32 bits do *ullArgument* em uma estrutura de **ponto** .</span><span class="sxs-lookup"><span data-stu-id="e3cad-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="e3cad-178">Indica a posição em que o primeiro dedo se resume.</span><span class="sxs-lookup"><span data-stu-id="e3cad-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="e3cad-179">Todas as distâncias e posições são fornecidas em coordenadas de tela físicas.</span><span class="sxs-lookup"><span data-stu-id="e3cad-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3cad-180">Os parâmetros *dwID* e *ullArgument* só devem ser considerados para acompanhar os \_ \* comandos GID e não devem ser alterados por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e3cad-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e3cad-181">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3cad-181">Examples</span></span>

<span data-ttu-id="e3cad-182">O código a seguir ilustra como obter informações específicas do gesto associadas a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e3cad-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="e3cad-183">Você sempre deve encaminhar mensagens sem tratamento para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) e deve fechar o manipulador de entrada de gesto para as mensagens que você manipula com uma chamada para [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span><span class="sxs-lookup"><span data-stu-id="e3cad-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="e3cad-184">Neste exemplo, o comportamento do manipulador de gestos padrão será suprimido porque o identificador TOUCHINPUT é fechado em cada um dos casos de gesto.</span><span class="sxs-lookup"><span data-stu-id="e3cad-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="e3cad-185">Se você removeu os casos no código acima para mensagens sem tratamento, o manipulador de gestos padrão processaria as mensagens sendo encaminhados para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) no caso padrão.</span><span class="sxs-lookup"><span data-stu-id="e3cad-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="e3cad-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cad-186">Requirements</span></span>



| <span data-ttu-id="e3cad-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cad-187">Requirement</span></span> | <span data-ttu-id="e3cad-188">Valor</span><span class="sxs-lookup"><span data-stu-id="e3cad-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cad-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cad-189">Minimum supported client</span></span><br/> | <span data-ttu-id="e3cad-190">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e3cad-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e3cad-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cad-191">Minimum supported server</span></span><br/> | <span data-ttu-id="e3cad-192">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e3cad-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e3cad-193">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3cad-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3cad-194"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3cad-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cad-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cad-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cad-196">Notificações</span><span class="sxs-lookup"><span data-stu-id="e3cad-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e3cad-197">Guia de programação de gestos do Windows Touch</span><span class="sxs-lookup"><span data-stu-id="e3cad-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

