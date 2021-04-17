---
description: Notifica um aplicativo quando um IME está prestes a criar a janela de status. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782798"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="756df-104">Código de notificação do IMN \_ OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="756df-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="756df-105">Notifica um aplicativo quando um IME está prestes a criar a janela de status.</span><span class="sxs-lookup"><span data-stu-id="756df-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="756df-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="756df-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="756df-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="756df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="756df-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="756df-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="756df-109">Defina como IMN \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="756df-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="756df-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="756df-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="756df-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="756df-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="756df-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="756df-112">Return Value</span></span>

<span data-ttu-id="756df-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="756df-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="756df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="756df-114">Remarks</span></span>

<span data-ttu-id="756df-115">Um aplicativo processa esse comando para exibir a janela de status do IME por si só.</span><span class="sxs-lookup"><span data-stu-id="756df-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="756df-116">A janela do IME cria uma janela de status quando processa esse comando e define as cadeias de caracteres a serem exibidas na janela para o contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="756df-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="756df-117">Os aplicativos podem obter informações sobre a janela de status usando a função [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="756df-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="756df-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756df-118">Requirements</span></span>



| <span data-ttu-id="756df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="756df-119">Requirement</span></span> | <span data-ttu-id="756df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="756df-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756df-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="756df-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="756df-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="756df-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="756df-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="756df-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="756df-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="756df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="756df-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="756df-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756df-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="756df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756df-128">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="756df-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="756df-129">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="756df-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="756df-130">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="756df-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="756df-131">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="756df-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




