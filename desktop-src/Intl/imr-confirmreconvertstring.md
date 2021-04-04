---
description: Notifica um aplicativo quando o IME precisa alterar a estrutura reconverterstring. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662153"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="25b52-104">Código de notificação do IMR \_ CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="25b52-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="25b52-105">Notifica um aplicativo quando o IME precisa alterar a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="25b52-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="25b52-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="25b52-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="25b52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25b52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b52-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="25b52-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="25b52-109">Defina como IMR \_ CONFIRMRECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="25b52-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="25b52-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="25b52-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="25b52-111">Ponteiro para uma estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) do IME.</span><span class="sxs-lookup"><span data-stu-id="25b52-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="25b52-112">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="25b52-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b52-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="25b52-113">Return Value</span></span>

<span data-ttu-id="25b52-114">Retorna um valor diferente de zero se o aplicativo aceita a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) alterada.</span><span class="sxs-lookup"><span data-stu-id="25b52-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="25b52-115">Caso contrário, o comando retornará 0 e o IME usará a estrutura **REconverterstring** original.</span><span class="sxs-lookup"><span data-stu-id="25b52-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b52-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="25b52-116">Remarks</span></span>

<span data-ttu-id="25b52-117">O aplicativo preenche a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) após receber o comando [IMR \_ reconverterstring](imr-reconvertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="25b52-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="25b52-118">Depois que o aplicativo tratou de [IMR \_ reconverterstring](imr-reconvertstring.md), o IME pode ou não ajustar a estrutura [**reconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="25b52-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="25b52-119">O IME envia a \_ solicitação de IME do WM \_ com o **IMR \_ CONFIRMRECONVERTSTRING** para confirmar as alterações na estrutura **reconverterstring** .</span><span class="sxs-lookup"><span data-stu-id="25b52-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="25b52-120">Se o aplicativo retornar **true** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **reconverterstring** para o comando **IMR \_ CONFIRMRECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="25b52-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="25b52-121">Se o aplicativo retornar **false** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **reconverterstring** original especificada pelo aplicativo no \_ comando IMR reconverterstring.</span><span class="sxs-lookup"><span data-stu-id="25b52-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b52-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25b52-122">Requirements</span></span>



| <span data-ttu-id="25b52-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b52-123">Requirement</span></span> | <span data-ttu-id="25b52-124">Valor</span><span class="sxs-lookup"><span data-stu-id="25b52-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b52-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25b52-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25b52-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25b52-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="25b52-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25b52-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25b52-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25b52-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25b52-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="25b52-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b52-130"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25b52-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b52-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="25b52-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b52-132">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="25b52-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="25b52-133">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="25b52-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="25b52-134">Reconverter de IMR \_</span><span class="sxs-lookup"><span data-stu-id="25b52-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="25b52-135">**Reconverterstring**</span><span class="sxs-lookup"><span data-stu-id="25b52-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="25b52-136">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="25b52-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




