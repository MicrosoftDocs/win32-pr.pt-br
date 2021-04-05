---
title: DM_POINTERHITTEST mensagem
description: Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para a manipulação direta.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- Mensagens de entrada e notificações de DM_POINTERHITTEST mensagem
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085950"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="8ea2b-104">DM_POINTERHITTEST mensagem</span><span class="sxs-lookup"><span data-stu-id="8ea2b-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="8ea2b-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="8ea2b-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ea2b-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="8ea2b-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ea2b-107">Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para a [manipulação direta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span><span class="sxs-lookup"><span data-stu-id="8ea2b-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="8ea2b-108">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="8ea2b-108">\[!Important\]</span></span>  
> <span data-ttu-id="8ea2b-109">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="8ea2b-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="8ea2b-110">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="8ea2b-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="8ea2b-111">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="8ea2b-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="8ea2b-112">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ea2b-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="8ea2b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ea2b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea2b-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ea2b-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea2b-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="8ea2b-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8ea2b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ea2b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea2b-117">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="8ea2b-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea2b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ea2b-118">Return value</span></span>

<span data-ttu-id="8ea2b-119">NULO</span><span class="sxs-lookup"><span data-stu-id="8ea2b-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea2b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea2b-120">Requirements</span></span>



| <span data-ttu-id="8ea2b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea2b-121">Requirement</span></span> | <span data-ttu-id="8ea2b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8ea2b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea2b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea2b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea2b-124">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8ea2b-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ea2b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea2b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea2b-126">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8ea2b-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ea2b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ea2b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea2b-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea2b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea2b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ea2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea2b-130">Mensagens</span><span class="sxs-lookup"><span data-stu-id="8ea2b-130">Messages</span></span>](messages.md)
</dt> </dl>

 

