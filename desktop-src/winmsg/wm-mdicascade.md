---
description: Um aplicativo envia a mensagem do WM \_ MDICASCADE para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas em um formato em cascata.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Mensagem de WM_MDICASCADE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296289"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="df3bc-103">Mensagem do WM \_ MDICASCADE</span><span class="sxs-lookup"><span data-stu-id="df3bc-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="df3bc-104">Um aplicativo envia a mensagem do **WM \_ MDICASCADE** para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas em um formato em cascata.</span><span class="sxs-lookup"><span data-stu-id="df3bc-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="df3bc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df3bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df3bc-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df3bc-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df3bc-107">O comportamento em cascata.</span><span class="sxs-lookup"><span data-stu-id="df3bc-107">The cascade behavior.</span></span> <span data-ttu-id="df3bc-108">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="df3bc-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="df3bc-109">Valor</span><span class="sxs-lookup"><span data-stu-id="df3bc-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="df3bc-110">Significado</span><span class="sxs-lookup"><span data-stu-id="df3bc-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="df3bc-111"><dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="df3bc-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="df3bc-112">Impede que janelas filho MDI desabilitadas sejam colocadas em cascata.</span><span class="sxs-lookup"><span data-stu-id="df3bc-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="df3bc-113"><dt>**MDITILE \_**</dt> <dt>0X0004</dt> de ZORDER</span><span class="sxs-lookup"><span data-stu-id="df3bc-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="df3bc-114">Organiza as janelas na ordem Z.</span><span class="sxs-lookup"><span data-stu-id="df3bc-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="df3bc-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df3bc-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df3bc-116">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="df3bc-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df3bc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df3bc-117">Return value</span></span>

<span data-ttu-id="df3bc-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="df3bc-118">Type: **BOOL**</span></span>

<span data-ttu-id="df3bc-119">Se a mensagem tiver sucesso, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="df3bc-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="df3bc-120">Se a mensagem falhar, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="df3bc-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df3bc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df3bc-121">Requirements</span></span>



| <span data-ttu-id="df3bc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df3bc-122">Requirement</span></span> | <span data-ttu-id="df3bc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df3bc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df3bc-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df3bc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df3bc-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df3bc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="df3bc-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df3bc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df3bc-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df3bc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df3bc-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df3bc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="df3bc-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df3bc-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3bc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="df3bc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="df3bc-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="df3bc-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="df3bc-132">**MDIICONARRANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="df3bc-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="df3bc-133">**MDITILE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="df3bc-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="df3bc-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="df3bc-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="df3bc-135">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="df3bc-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




