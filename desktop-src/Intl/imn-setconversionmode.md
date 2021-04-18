---
description: Notifica um aplicativo quando o modo de conversão do contexto de entrada é atualizado. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: IMN_SETCONVERSIONMODE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810335"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="4e850-104">\_Código de notificação IMN SETconversionmode</span><span class="sxs-lookup"><span data-stu-id="4e850-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="4e850-105">Notifica um aplicativo quando o modo de conversão do contexto de entrada é atualizado.</span><span class="sxs-lookup"><span data-stu-id="4e850-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="4e850-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="4e850-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="4e850-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e850-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e850-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e850-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4e850-109">Defina como IMN \_ SETconversionmode.</span><span class="sxs-lookup"><span data-stu-id="4e850-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="4e850-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e850-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4e850-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4e850-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e850-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4e850-112">Return Value</span></span>

<span data-ttu-id="4e850-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4e850-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e850-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e850-114">Remarks</span></span>

<span data-ttu-id="4e850-115">O aplicativo pode obter informações sobre o modo de conversão usando a função [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="4e850-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e850-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e850-116">Requirements</span></span>



| <span data-ttu-id="4e850-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e850-117">Requirement</span></span> | <span data-ttu-id="4e850-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4e850-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e850-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e850-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e850-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e850-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4e850-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e850-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e850-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e850-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e850-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e850-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e850-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e850-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e850-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e850-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e850-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="4e850-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4e850-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="4e850-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4e850-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="4e850-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="4e850-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4e850-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




