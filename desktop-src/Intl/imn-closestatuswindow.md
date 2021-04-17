---
description: Notifica um aplicativo quando um IME está prestes a fechar a janela de status. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747795"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="f0b26-104">Código de notificação do IMN \_ CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="f0b26-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="f0b26-105">Notifica um aplicativo quando um IME está prestes a fechar a janela de status.</span><span class="sxs-lookup"><span data-stu-id="f0b26-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="f0b26-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="f0b26-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="f0b26-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0b26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b26-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0b26-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f0b26-109">Defina como IMN \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="f0b26-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="f0b26-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0b26-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f0b26-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f0b26-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b26-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f0b26-112">Return Value</span></span>

<span data-ttu-id="f0b26-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f0b26-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b26-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0b26-114">Remarks</span></span>

<span data-ttu-id="f0b26-115">Um aplicativo deve processar esse comando se ele exibir a janela de status do IME.</span><span class="sxs-lookup"><span data-stu-id="f0b26-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="f0b26-116">A janela do IME fecha a janela de status ao processar esse comando.</span><span class="sxs-lookup"><span data-stu-id="f0b26-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b26-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0b26-117">Requirements</span></span>



| <span data-ttu-id="f0b26-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0b26-118">Requirement</span></span> | <span data-ttu-id="f0b26-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f0b26-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b26-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0b26-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b26-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0b26-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f0b26-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0b26-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b26-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0b26-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0b26-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f0b26-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b26-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0b26-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b26-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0b26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b26-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f0b26-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f0b26-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f0b26-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f0b26-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f0b26-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




