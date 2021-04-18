---
description: Notifica um aplicativo quando a fonte do contexto de entrada é atualizada. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778575"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="2ed53-104">Código de notificação do IMN \_ SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="2ed53-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="2ed53-105">Notifica um aplicativo quando a fonte do contexto de entrada é atualizada.</span><span class="sxs-lookup"><span data-stu-id="2ed53-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="2ed53-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="2ed53-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="2ed53-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ed53-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ed53-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ed53-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2ed53-109">Defina como IMN \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="2ed53-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="2ed53-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ed53-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2ed53-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2ed53-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ed53-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2ed53-112">Return Value</span></span>

<span data-ttu-id="2ed53-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2ed53-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed53-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ed53-114">Remarks</span></span>

<span data-ttu-id="2ed53-115">O aplicativo pode obter informações sobre a fonte usando a função [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) .</span><span class="sxs-lookup"><span data-stu-id="2ed53-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="2ed53-116">A janela do IME subseqüentemente usa a fonte para desenhar a cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="2ed53-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed53-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ed53-117">Requirements</span></span>



| <span data-ttu-id="2ed53-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed53-118">Requirement</span></span> | <span data-ttu-id="2ed53-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2ed53-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed53-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ed53-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed53-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ed53-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ed53-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ed53-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed53-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ed53-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2ed53-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ed53-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ed53-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed53-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed53-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ed53-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed53-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2ed53-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2ed53-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2ed53-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2ed53-129">**ImmGetCompositionFont**</span><span class="sxs-lookup"><span data-stu-id="2ed53-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="2ed53-130">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2ed53-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




