---
description: Usado para definir mensagens privadas, geralmente do formulário WM \_ app + x, em que x é um valor inteiro.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170451"
---
# <a name="wm_app"></a><span data-ttu-id="173f3-103">aplicativo do WM \_</span><span class="sxs-lookup"><span data-stu-id="173f3-103">WM\_APP</span></span>

<span data-ttu-id="173f3-104">Usado para definir mensagens privadas, geralmente do formulário **WM \_ app** + *x*, em que *x* é um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="173f3-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="173f3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="173f3-105">Remarks</span></span>

<span data-ttu-id="173f3-106">A constante do **\_ aplicativo do WM** é usada para distinguir os valores de mensagem que estão reservados para uso pelo sistema e os valores que podem ser usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada.</span><span class="sxs-lookup"><span data-stu-id="173f3-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="173f3-107">A seguir estão os intervalos de números de mensagem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="173f3-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="173f3-108">Intervalo</span><span class="sxs-lookup"><span data-stu-id="173f3-108">Range</span></span>                                                 | <span data-ttu-id="173f3-109">Significado</span><span class="sxs-lookup"><span data-stu-id="173f3-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="173f3-110">0 por meio do [**\_ usuário do WM**](wm-user.md) – 1</span><span class="sxs-lookup"><span data-stu-id="173f3-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="173f3-111">Mensagens reservadas para uso pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="173f3-112">[**WM \_ USUÁRIO**](wm-user.md) por meio de 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="173f3-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="173f3-113">Mensagens de inteiros para uso por classes de janela privada.</span><span class="sxs-lookup"><span data-stu-id="173f3-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="173f3-114">**WM \_ APLICATIVO** por meio de 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="173f3-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="173f3-115">Mensagens disponíveis para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="173f3-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="173f3-116">0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="173f3-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="173f3-117">Mensagens de cadeia de caracteres para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="173f3-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="173f3-118">Maior que 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="173f3-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="173f3-119">Reservado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="173f3-120">Os números de mensagem no primeiro intervalo (0 [**por \_ usuário do WM**](wm-user.md) – 1) são definidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="173f3-121">Os valores neste intervalo que não são definidos explicitamente são reservados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="173f3-122">Os números de mensagem no segundo intervalo [**( \_ usuário do WM**](wm-user.md) por meio de 0x7FFF) podem ser definidos e usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada.</span><span class="sxs-lookup"><span data-stu-id="173f3-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="173f3-123">Esses valores não podem ser usados para definir mensagens que são significativas em um aplicativo porque algumas classes de janela predefinidas já definem valores nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="173f3-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="173f3-124">Por exemplo, classes de controle predefinidas como **Button**, **Edit**, **ListBox** e **ComboBox** podem usar esses valores.</span><span class="sxs-lookup"><span data-stu-id="173f3-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="173f3-125">As mensagens neste intervalo não devem ser enviadas a outros aplicativos, a menos que os aplicativos tenham sido projetados para trocar mensagens e para anexar o mesmo significado aos números de mensagem.</span><span class="sxs-lookup"><span data-stu-id="173f3-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="173f3-126">Os números de mensagem no terceiro intervalo (0x8000 a 0xBFFF) estão disponíveis para que os aplicativos usem como mensagens privadas.</span><span class="sxs-lookup"><span data-stu-id="173f3-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="173f3-127">As mensagens neste intervalo não entram em conflito com as mensagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="173f3-128">Os números de mensagem no quarto intervalo (0xC000 a 0xFFFF) são definidos em tempo de execução quando um aplicativo chama a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar um número de mensagem para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="173f3-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="173f3-129">Todos os aplicativos que registram a mesma cadeia de caracteres podem usar o número de mensagem associado para troca de mensagens.</span><span class="sxs-lookup"><span data-stu-id="173f3-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="173f3-130">No entanto, o número da mensagem real não é uma constante e não pode ser considerado o mesmo entre sessões diferentes.</span><span class="sxs-lookup"><span data-stu-id="173f3-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="173f3-131">Os números de mensagem no quinto intervalo (maior que 0xFFFF) são reservados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="173f3-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="173f3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="173f3-132">Requirements</span></span>



| <span data-ttu-id="173f3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="173f3-133">Requirement</span></span> | <span data-ttu-id="173f3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="173f3-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173f3-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="173f3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="173f3-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="173f3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="173f3-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="173f3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="173f3-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="173f3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="173f3-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="173f3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="173f3-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="173f3-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="173f3-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="173f3-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="173f3-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="173f3-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="173f3-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="173f3-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="173f3-144">**usuário do WM \_**</span><span class="sxs-lookup"><span data-stu-id="173f3-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="173f3-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="173f3-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="173f3-146">Mensagens e filas de mensagens</span><span class="sxs-lookup"><span data-stu-id="173f3-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
