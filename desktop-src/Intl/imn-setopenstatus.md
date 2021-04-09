---
description: Notifica um aplicativo quando o status de abertura do contexto de entrada é atualizado. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010998"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="d5eda-104">Código de notificação do IMN \_ SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="d5eda-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="d5eda-105">Notifica um aplicativo quando o status de abertura do contexto de entrada é atualizado.</span><span class="sxs-lookup"><span data-stu-id="d5eda-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="d5eda-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="d5eda-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="d5eda-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5eda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5eda-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5eda-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d5eda-109">Defina como IMN \_ SETOPENSTATUS.</span><span class="sxs-lookup"><span data-stu-id="d5eda-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="d5eda-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5eda-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d5eda-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d5eda-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5eda-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d5eda-112">Return Value</span></span>

<span data-ttu-id="d5eda-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d5eda-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5eda-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5eda-114">Remarks</span></span>

<span data-ttu-id="d5eda-115">O aplicativo pode obter informações sobre o status aberto usando a função [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .</span><span class="sxs-lookup"><span data-stu-id="d5eda-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5eda-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5eda-116">Requirements</span></span>



| <span data-ttu-id="d5eda-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5eda-117">Requirement</span></span> | <span data-ttu-id="d5eda-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d5eda-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5eda-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5eda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5eda-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5eda-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5eda-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5eda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5eda-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5eda-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d5eda-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d5eda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5eda-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5eda-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5eda-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5eda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5eda-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5eda-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d5eda-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5eda-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d5eda-128">**ImmGetOpenStatus**</span><span class="sxs-lookup"><span data-stu-id="d5eda-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="d5eda-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d5eda-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




