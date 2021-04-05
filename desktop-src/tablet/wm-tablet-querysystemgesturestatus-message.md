---
description: Enviado quando o sistema solicita uma janela que os gestos do sistema desejam receber.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Mensagem de WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827072"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="7a1d8-103">\_Mensagem de Tablet QUERYSYSTEMGESTURESTATUS do WM \_</span><span class="sxs-lookup"><span data-stu-id="7a1d8-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="7a1d8-104">Enviado quando o sistema solicita uma janela que os gestos do sistema desejam receber.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="7a1d8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a1d8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a1d8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a1d8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a1d8-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7a1d8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a1d8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a1d8-109">Um valor de ponto que representa as coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a1d8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a1d8-110">Remarks</span></span>

<span data-ttu-id="7a1d8-111">Ao lidar com essa mensagem, você pode desabilitar dinamicamente os movimentos de regiões de uma janela.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="7a1d8-112">O *lParam* pode ser convertido em coordenadas x e em coordenadas y usando as `GET_X_LPARAM` `GET_Y_LPARAM` macros e.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="7a1d8-113">Por padrão, sua janela receberá todos os eventos de gesto do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="7a1d8-114">Você pode escolher quais eventos deseja que sua janela receba e quais eventos você gostaria de desabilitar respondendo à mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** em seu **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="7a1d8-115">A mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** é definida em tpcshrd. h.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="7a1d8-116">Os valores para habilitar e desabilitar gestos do sistema Tablet System também são definidos em tpcshrd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7a1d8-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> <span data-ttu-id="7a1d8-117">Desabilitar a operação de pressionar e manter irá melhorar a capacidade de resposta para cliques do mouse, pois essa funcionalidade cria um tempo de espera para distinguir entre as duas operações.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="7a1d8-118">Tenha cuidado ao manipular a mensagem de **\_ Tablet \_ QUERYSYSTEMGESTURESTATUS do WM** .</span><span class="sxs-lookup"><span data-stu-id="7a1d8-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="7a1d8-119">**WM \_ O TABLET \_ QUERYSYSTEMGESTURESTATUS** é passado usando a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="7a1d8-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="7a1d8-120">Se você chamar métodos em uma interface COM, esse objeto deverá estar dentro do mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="7a1d8-121">Caso contrário, COM gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="7a1d8-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a1d8-122">Examples</span></span>

<span data-ttu-id="7a1d8-123">O exemplo a seguir mostra como desabilitar movimentos para uma região usando o WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



<span data-ttu-id="7a1d8-124">O exemplo a seguir mostra como desabilitar vários recursos de movimentos para uma janela inteira.</span><span class="sxs-lookup"><span data-stu-id="7a1d8-124">The following example shows how to disable various flicks features for an entire window.</span></span>


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a><span data-ttu-id="7a1d8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a1d8-125">Requirements</span></span>



| <span data-ttu-id="7a1d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a1d8-126">Requirement</span></span> | <span data-ttu-id="7a1d8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7a1d8-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1d8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a1d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1d8-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a1d8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7a1d8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a1d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1d8-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a1d8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a1d8-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a1d8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a1d8-133"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a1d8-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
