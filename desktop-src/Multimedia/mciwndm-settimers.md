---
title: Mensagem de MCIWNDM_SETTIMERS (VFW. h)
description: A \_ mensagem SETtimers MCIWNDM define os períodos de atualização usados pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETTIMERS
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644333"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="21cdb-104">\_Mensagem SETtimers MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="21cdb-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="21cdb-105">A **mensagem \_ settimers MCIWNDM** define os períodos de atualização usados pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="21cdb-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="21cdb-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="21cdb-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="21cdb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21cdb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cdb-108"><span id="active"></span><span id="ACTIVE"></span>*activo*</span><span class="sxs-lookup"><span data-stu-id="21cdb-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="21cdb-109">Período de atualização usado pelo MCIWnd quando é a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="21cdb-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="21cdb-110">O valor padrão é 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="21cdb-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="21cdb-111">O armazenamento para esse valor é limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="21cdb-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="21cdb-112"><span id="inactive"></span><span id="INACTIVE"></span>*inativo*</span><span class="sxs-lookup"><span data-stu-id="21cdb-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="21cdb-113">Período de atualização usado pelo MCIWnd quando é a janela inativa.</span><span class="sxs-lookup"><span data-stu-id="21cdb-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="21cdb-114">O valor padrão é 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="21cdb-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="21cdb-115">O armazenamento para esse valor é limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="21cdb-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cdb-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="21cdb-116">Return Value</span></span>

<span data-ttu-id="21cdb-117">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="21cdb-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21cdb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21cdb-118">Requirements</span></span>



| <span data-ttu-id="21cdb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="21cdb-119">Requirement</span></span> | <span data-ttu-id="21cdb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="21cdb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21cdb-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21cdb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21cdb-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21cdb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="21cdb-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21cdb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21cdb-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21cdb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21cdb-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21cdb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="21cdb-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="21cdb-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21cdb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="21cdb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cdb-128">**MCIWndSetTimers**</span><span class="sxs-lookup"><span data-stu-id="21cdb-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





