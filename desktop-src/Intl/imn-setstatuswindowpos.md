---
description: Notifica um aplicativo quando a posição da janela de status no contexto de entrada é atualizada. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro da seguinte maneira.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: IMN_SETSTATUSWINDOWPOS código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760847"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="4ca38-104">Código de notificação do IMN \_ SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="4ca38-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="4ca38-105">Notifica um aplicativo quando a posição da janela de status no contexto de entrada é atualizada.</span><span class="sxs-lookup"><span data-stu-id="4ca38-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="4ca38-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="4ca38-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="4ca38-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca38-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ca38-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4ca38-109">Defina como IMN \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="4ca38-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="4ca38-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ca38-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4ca38-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4ca38-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca38-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4ca38-112">Return Value</span></span>

<span data-ttu-id="4ca38-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4ca38-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca38-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca38-114">Remarks</span></span>

<span data-ttu-id="4ca38-115">O aplicativo pode obter informações sobre a posição da janela de status usando o comando [**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca38-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca38-116">Requirements</span></span>



| <span data-ttu-id="4ca38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca38-117">Requirement</span></span> | <span data-ttu-id="4ca38-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca38-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca38-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca38-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ca38-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ca38-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca38-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ca38-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ca38-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4ca38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca38-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ca38-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca38-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca38-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="4ca38-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4ca38-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="4ca38-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4ca38-128">**GETSTATUSWINDOWPOS do IMC \_**</span><span class="sxs-lookup"><span data-stu-id="4ca38-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="4ca38-129">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ca38-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




