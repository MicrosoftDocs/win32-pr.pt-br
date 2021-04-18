---
description: Enviado a todas as janelas de nível superior quando o sistema detecta mais de 12,5 por cento do tempo do sistema em um intervalo de 30 a 60 segundos está sendo gasto com a compactação da memória. Isso indica que a memória do sistema está baixa.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Mensagem de WM_COMPACTING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786213"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="5d1f0-104">\_Mensagem de compactação do WM</span><span class="sxs-lookup"><span data-stu-id="5d1f0-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="5d1f0-105">Enviado a todas as janelas de nível superior quando o sistema detecta mais de 12,5 por cento do tempo do sistema em um intervalo de 30 a 60 segundos está sendo gasto com a compactação da memória.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="5d1f0-106">Isso indica que a memória do sistema está baixa.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="5d1f0-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5d1f0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="5d1f0-108">Essa mensagem é fornecida apenas para compatibilidade com aplicativos baseados no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="5d1f0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d1f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d1f0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d1f0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d1f0-111">A proporção do tempo de CPU (unidade de processamento central) gasto atualmente pela compactação da memória do sistema para o tempo de CPU atualmente gasto pelo sistema executando outras operações.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="5d1f0-112">Por exemplo, 0x8000 representa 50% do tempo de CPU gasto na compactação da memória.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="5d1f0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d1f0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d1f0-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d1f0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d1f0-115">Return value</span></span>

<span data-ttu-id="5d1f0-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d1f0-116">Type: **LRESULT**</span></span>

<span data-ttu-id="5d1f0-117">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d1f0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d1f0-118">Remarks</span></span>

<span data-ttu-id="5d1f0-119">Quando um aplicativo recebe essa mensagem, ele deve liberar o máximo de memória possível, levando em conta o nível atual de atividade do aplicativo e o número total de aplicativos em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="5d1f0-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1f0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d1f0-120">Requirements</span></span>



| <span data-ttu-id="5d1f0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d1f0-121">Requirement</span></span> | <span data-ttu-id="5d1f0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5d1f0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1f0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d1f0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5d1f0-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d1f0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d1f0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d1f0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5d1f0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d1f0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d1f0-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d1f0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d1f0-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d1f0-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d1f0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d1f0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1f0-130">Visão geral do Windows</span><span class="sxs-lookup"><span data-stu-id="5d1f0-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
