---
description: Notifica um aplicativo quando um IME está prestes a mostrar uma mensagem de erro ou outras informações. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296802"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="1fcc1-104">Código de notificação de diretriz de IMN \_</span><span class="sxs-lookup"><span data-stu-id="1fcc1-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="1fcc1-105">Notifica um aplicativo quando um IME está prestes a mostrar uma mensagem de erro ou outras informações.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="1fcc1-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="1fcc1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fcc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcc1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fcc1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1fcc1-109">Defina como diretriz de IMN \_ .</span><span class="sxs-lookup"><span data-stu-id="1fcc1-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="1fcc1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fcc1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1fcc1-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcc1-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1fcc1-112">Return Value</span></span>

<span data-ttu-id="1fcc1-113">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcc1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fcc1-114">Remarks</span></span>

<span data-ttu-id="1fcc1-115">Um aplicativo processa esse comando chamando a função [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) para recuperar a mensagem de erro ou as informações do IME.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="1fcc1-116">A janela IME exibe a mensagem de erro ou a cadeia de informações em uma janela de informações.</span><span class="sxs-lookup"><span data-stu-id="1fcc1-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcc1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcc1-117">Requirements</span></span>



| <span data-ttu-id="1fcc1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcc1-118">Requirement</span></span> | <span data-ttu-id="1fcc1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1fcc1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcc1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fcc1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcc1-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1fcc1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1fcc1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fcc1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcc1-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1fcc1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fcc1-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1fcc1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcc1-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fcc1-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcc1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fcc1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcc1-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1fcc1-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1fcc1-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1fcc1-129">**ImmGetGuideLine**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="1fcc1-130">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1fcc1-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




