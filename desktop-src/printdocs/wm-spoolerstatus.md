---
description: A mensagem do WM \_ SPOOLERSTATUS é enviada do Gerenciador de impressão sempre que um trabalho é adicionado ou removido da fila do Gerenciador de impressão.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Mensagem de WM_SPOOLERSTATUS (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091697"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="43c0d-103">Mensagem do WM \_ SPOOLERSTATUS</span><span class="sxs-lookup"><span data-stu-id="43c0d-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="43c0d-104">A mensagem do **WM \_ SPOOLERSTATUS** é enviada do Gerenciador de impressão sempre que um trabalho é adicionado ou removido da fila do Gerenciador de impressão.</span><span class="sxs-lookup"><span data-stu-id="43c0d-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="43c0d-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="43c0d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="43c0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43c0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c0d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43c0d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43c0d-108">O \_ sinalizador PR JOBSTATUS.</span><span class="sxs-lookup"><span data-stu-id="43c0d-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="43c0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43c0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43c0d-110">A palavra de ordem inferior Especifica o número de trabalhos restantes na fila do Gerenciador de impressão.</span><span class="sxs-lookup"><span data-stu-id="43c0d-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c0d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43c0d-111">Return value</span></span>

<span data-ttu-id="43c0d-112">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="43c0d-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c0d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="43c0d-113">Remarks</span></span>

<span data-ttu-id="43c0d-114">Esta mensagem é apenas para fins informativos.</span><span class="sxs-lookup"><span data-stu-id="43c0d-114">This message is for informational purposes only.</span></span> <span data-ttu-id="43c0d-115">Esta mensagem é consultoria e não tem semântica de entrega garantida.</span><span class="sxs-lookup"><span data-stu-id="43c0d-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="43c0d-116">Os aplicativos não devem pressupor que receberão uma \_ mensagem do WM SPOOLERSTATUS para cada alteração no status do spooler.</span><span class="sxs-lookup"><span data-stu-id="43c0d-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="43c0d-117">A mensagem do WM \_ SPOOLERSTATUS não tem suporte após o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="43c0d-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="43c0d-118">Para ser notificado sobre alterações no status da fila de impressão, você pode usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) e [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="43c0d-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43c0d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43c0d-119">Requirements</span></span>



| <span data-ttu-id="43c0d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c0d-120">Requirement</span></span> | <span data-ttu-id="43c0d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="43c0d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c0d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c0d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="43c0d-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43c0d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43c0d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c0d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="43c0d-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43c0d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43c0d-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43c0d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c0d-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43c0d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c0d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="43c0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c0d-129">Impressão</span><span class="sxs-lookup"><span data-stu-id="43c0d-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="43c0d-130">Mensagens da API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="43c0d-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="43c0d-131">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="43c0d-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="43c0d-132">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="43c0d-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

