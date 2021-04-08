---
description: Notifica um aplicativo quando um IME selecionado precisa de uma cadeia de caracteres para a reconversão. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828271"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="bd369-104">\_Código de notificação de REconversão de IMR</span><span class="sxs-lookup"><span data-stu-id="bd369-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="bd369-105">Notifica um aplicativo quando um IME selecionado precisa de uma cadeia de caracteres para a reconversão.</span><span class="sxs-lookup"><span data-stu-id="bd369-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="bd369-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="bd369-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="bd369-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd369-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd369-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd369-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="bd369-109">Defina como \_ Reconverter de IMR.</span><span class="sxs-lookup"><span data-stu-id="bd369-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="bd369-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd369-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="bd369-111">Ponteiro para um buffer que contém a estrutura de [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) e cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd369-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd369-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bd369-112">Return Value</span></span>

<span data-ttu-id="bd369-113">Retorna a estrutura da cadeia de caracteres de reconversão atual.</span><span class="sxs-lookup"><span data-stu-id="bd369-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="bd369-114">Se *lParam* for definido como **NULL**, o aplicativo retornará o tamanho do buffer necessário para manter a estrutura.</span><span class="sxs-lookup"><span data-stu-id="bd369-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="bd369-115">O comando retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="bd369-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd369-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd369-116">Requirements</span></span>



| <span data-ttu-id="bd369-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd369-117">Requirement</span></span> | <span data-ttu-id="bd369-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bd369-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd369-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd369-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd369-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd369-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd369-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd369-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd369-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd369-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd369-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd369-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd369-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd369-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd369-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd369-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd369-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="bd369-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="bd369-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="bd369-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="bd369-128">**Reconverterstring**</span><span class="sxs-lookup"><span data-stu-id="bd369-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="bd369-129">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bd369-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




