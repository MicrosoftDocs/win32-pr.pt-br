---
description: Notifica um aplicativo quando o estilo ou a posição da janela de composição é atualizada. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922547"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="2e7df-104">Código de notificação do IMN \_ SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="2e7df-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="2e7df-105">Notifica um aplicativo quando o estilo ou a posição da janela de composição é atualizada.</span><span class="sxs-lookup"><span data-stu-id="2e7df-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="2e7df-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="2e7df-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="2e7df-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e7df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7df-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e7df-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2e7df-109">Defina como IMN \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="2e7df-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="2e7df-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e7df-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2e7df-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2e7df-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7df-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2e7df-112">Return Value</span></span>

<span data-ttu-id="2e7df-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2e7df-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e7df-114">Remarks</span></span>

<span data-ttu-id="2e7df-115">O aplicativo pode obter informações sobre o formulário de composição usando o comando [**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="2e7df-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7df-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e7df-116">Requirements</span></span>



| <span data-ttu-id="2e7df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e7df-117">Requirement</span></span> | <span data-ttu-id="2e7df-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2e7df-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7df-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e7df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7df-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2e7df-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2e7df-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e7df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7df-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2e7df-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e7df-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2e7df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e7df-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e7df-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7df-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e7df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7df-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2e7df-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2e7df-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2e7df-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2e7df-128">**GETCOMPOSITIONWINDOW do IMC \_**</span><span class="sxs-lookup"><span data-stu-id="2e7df-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="2e7df-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2e7df-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




