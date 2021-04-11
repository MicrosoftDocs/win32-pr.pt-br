---
description: Enviado quando um usuário executa um movimento de caneta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Mensagem de WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164429"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="884ba-104">Mensagem de movimento do \_ Tablet do WM \_</span><span class="sxs-lookup"><span data-stu-id="884ba-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="884ba-105">Enviado quando um usuário executa um movimento de caneta.</span><span class="sxs-lookup"><span data-stu-id="884ba-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="884ba-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="884ba-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="884ba-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="884ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884ba-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="884ba-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="884ba-109">Uma [**\_ estrutura de dados de movimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) que contém informações sobre o movimento de caneta que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="884ba-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="884ba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="884ba-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="884ba-111">A [**\_ estrutura do ponto de movimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) que especifica onde ocorreu o movimento da caneta.</span><span class="sxs-lookup"><span data-stu-id="884ba-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="884ba-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="884ba-112">Remarks</span></span>

<span data-ttu-id="884ba-113">Um movimento de caneta é um gesto de caneta unidirecional que exige que o usuário contate o digitalizador em um movimento de movimentos rápido e reto.</span><span class="sxs-lookup"><span data-stu-id="884ba-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="884ba-114">Um movimento é caracterizado por alta velocidade e um alto grau de reta.</span><span class="sxs-lookup"><span data-stu-id="884ba-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="884ba-115">Um movimento é identificado pela sua direção.</span><span class="sxs-lookup"><span data-stu-id="884ba-115">A flick is identified by its direction.</span></span> <span data-ttu-id="884ba-116">Os movimentos podem ser feitos em oito direções correspondentes às direções cardeal e secundária Compass.</span><span class="sxs-lookup"><span data-stu-id="884ba-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="884ba-117">Quando ocorre um movimento de caneta, o Windows primeiro notifica um aplicativo enviando uma mensagem de **\_ \_ movimento de Tablet do WM** , que uma janela recebe por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="884ba-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="884ba-118">Retorne a constante de **movimento \_ \_ manipulada \_ pelo WM** , descrita em constantes de [movimentos](flicks-constants.md), para indicar que o aplicativo respondeu à mensagem de **\_ \_ movimento de Tablet do WM** .</span><span class="sxs-lookup"><span data-stu-id="884ba-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="884ba-119">Se o aplicativo não retornar a **\_ \_ \_ máscara manipulada do WM de movimento**, o Windows executará a ação padrão especificada no painel de controle de movimentos enviando uma notificação de acompanhamento, como o [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), o [**WM \_ VSCROLL**](../controls/wm-vscroll.md)ou o [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md), dependendo de qual ação está associada ao movimento da caneta.</span><span class="sxs-lookup"><span data-stu-id="884ba-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="884ba-120">Tenha cuidado ao manipular a mensagem de **\_ \_ Tablet do WM** .</span><span class="sxs-lookup"><span data-stu-id="884ba-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="884ba-121">**WM \_ O \_ movimento do Tablet** é passado por meio da função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="884ba-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="884ba-122">Se você chamar métodos em uma interface COM, esse objeto deverá estar dentro do mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="884ba-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="884ba-123">Caso contrário, COM gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="884ba-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="884ba-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="884ba-124">Requirements</span></span>



| <span data-ttu-id="884ba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="884ba-125">Requirement</span></span> | <span data-ttu-id="884ba-126">Valor</span><span class="sxs-lookup"><span data-stu-id="884ba-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="884ba-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="884ba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="884ba-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="884ba-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="884ba-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="884ba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="884ba-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="884ba-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="884ba-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="884ba-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="884ba-132"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="884ba-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884ba-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="884ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884ba-134">**mover \_ estrutura de dados**</span><span class="sxs-lookup"><span data-stu-id="884ba-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="884ba-135">**mensagem de movimento do \_ Tablet do WM \_**</span><span class="sxs-lookup"><span data-stu-id="884ba-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="884ba-136">gestos de movimentos</span><span class="sxs-lookup"><span data-stu-id="884ba-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="884ba-137">[respondendo a movimentos de caneta](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="884ba-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
