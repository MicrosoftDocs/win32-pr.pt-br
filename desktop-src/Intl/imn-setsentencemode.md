---
description: Notifica um aplicativo quando o modo de sentença do contexto de entrada é atualizado. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: IMN_SETSENTENCEMODE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0130c5b3d7284112e64cca698b358650f51f3642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787518"
---
# <a name="imn_setsentencemode-notification-code"></a><span data-ttu-id="1fca0-104">\_Código de notificação IMN SETfrasemode</span><span class="sxs-lookup"><span data-stu-id="1fca0-104">IMN\_SETSENTENCEMODE notification code</span></span>

<span data-ttu-id="1fca0-105">Notifica um aplicativo quando o modo de sentença do contexto de entrada é atualizado.</span><span class="sxs-lookup"><span data-stu-id="1fca0-105">Notifies an application when the sentence mode of the input context is updated.</span></span> <span data-ttu-id="1fca0-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="1fca0-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a><span data-ttu-id="1fca0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fca0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fca0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fca0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1fca0-109">Defina como IMN \_ SETsentençamode.</span><span class="sxs-lookup"><span data-stu-id="1fca0-109">Set to IMN\_SETSENTENCEMODE.</span></span>

</dd> <dt>

<span data-ttu-id="1fca0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fca0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1fca0-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1fca0-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fca0-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1fca0-112">Return Value</span></span>

<span data-ttu-id="1fca0-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1fca0-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fca0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fca0-114">Remarks</span></span>

<span data-ttu-id="1fca0-115">O aplicativo pode obter informações sobre o modo de frase usando a função [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="1fca0-115">The application can get information about the sentence mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fca0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fca0-116">Requirements</span></span>



| <span data-ttu-id="1fca0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fca0-117">Requirement</span></span> | <span data-ttu-id="1fca0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1fca0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fca0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fca0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1fca0-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1fca0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1fca0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fca0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1fca0-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1fca0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fca0-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1fca0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fca0-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fca0-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fca0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fca0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fca0-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1fca0-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1fca0-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1fca0-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1fca0-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="1fca0-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="1fca0-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1fca0-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




