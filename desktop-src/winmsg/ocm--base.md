---
description: Usado para definir mensagens privadas para uso por classes de janela privada, geralmente no formato OCM \_ \_ base + x, em que x é um valor inteiro.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (OLECTL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc79cc842a7f25ba66dc8d807c5ab355fc04547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797959"
---
# <a name="ocm__base"></a><span data-ttu-id="61bc4-103">\_ \_ base OCM</span><span class="sxs-lookup"><span data-stu-id="61bc4-103">OCM\_\_BASE</span></span>

<span data-ttu-id="61bc4-104">Usado para definir mensagens privadas para uso por classes de janela privada, geralmente no formato **OCM \_ \_ base** + *x*, em que *x* é um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="61bc4-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="61bc4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="61bc4-105">Remarks</span></span>

<span data-ttu-id="61bc4-106">A seguir estão os intervalos de números de mensagem.</span><span class="sxs-lookup"><span data-stu-id="61bc4-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="61bc4-107">Intervalo</span><span class="sxs-lookup"><span data-stu-id="61bc4-107">Range</span></span>                                                 | <span data-ttu-id="61bc4-108">Significado</span><span class="sxs-lookup"><span data-stu-id="61bc4-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="61bc4-109">0 a [**WM \_ usuário**](wm-user.md)  1</span><span class="sxs-lookup"><span data-stu-id="61bc4-109">0 through [**WM\_USER**](wm-user.md)  1</span></span><br/>   | <span data-ttu-id="61bc4-110">Mensagens reservadas para uso pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="61bc4-111">[**WM \_ USUÁRIO**](wm-user.md) por meio de 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="61bc4-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="61bc4-112">Mensagens de inteiros para uso por classes de janela privada.</span><span class="sxs-lookup"><span data-stu-id="61bc4-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="61bc4-113">[**WM \_ APLICATIVO**](wm-app.md) por meio de 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="61bc4-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="61bc4-114">Mensagens disponíveis para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61bc4-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="61bc4-115">0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="61bc4-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="61bc4-116">Mensagens de cadeia de caracteres para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61bc4-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="61bc4-117">Maior que 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="61bc4-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="61bc4-118">Reservado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="61bc4-119">Os números de mensagem no primeiro intervalo (0 [**por \_ usuário do WM**](wm-user.md)  1) são definidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="61bc4-120">Os valores neste intervalo que não são definidos explicitamente são reservados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="61bc4-121">Os números de mensagem no segundo intervalo [**( \_ usuário do WM**](wm-user.md) por meio de 0x7FFF) podem ser definidos e usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada.</span><span class="sxs-lookup"><span data-stu-id="61bc4-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="61bc4-122">Esses valores não podem ser usados para definir mensagens que são significativas em um aplicativo porque algumas classes de janela predefinidas já definem valores nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="61bc4-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="61bc4-123">Por exemplo, classes de controle predefinidas como **Button**, **Edit**, **ListBox** e **ComboBox** podem usar esses valores.</span><span class="sxs-lookup"><span data-stu-id="61bc4-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="61bc4-124">As mensagens neste intervalo não devem ser enviadas a outros aplicativos, a menos que os aplicativos tenham sido projetados para trocar mensagens e para anexar o mesmo significado aos números de mensagem.</span><span class="sxs-lookup"><span data-stu-id="61bc4-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="61bc4-125">Os números de mensagem no terceiro intervalo (0x8000 a 0xBFFF) estão disponíveis para que os aplicativos usem como mensagens privadas.</span><span class="sxs-lookup"><span data-stu-id="61bc4-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="61bc4-126">As mensagens neste intervalo não entram em conflito com as mensagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="61bc4-127">Os números de mensagem no quarto intervalo (0xC000 a 0xFFFF) são definidos em tempo de execução quando um aplicativo chama a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar um número de mensagem para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="61bc4-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="61bc4-128">Todos os aplicativos que registram a mesma cadeia de caracteres podem usar o número de mensagem associado para troca de mensagens.</span><span class="sxs-lookup"><span data-stu-id="61bc4-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="61bc4-129">No entanto, o número da mensagem real não é uma constante e não pode ser considerado o mesmo entre sessões diferentes.</span><span class="sxs-lookup"><span data-stu-id="61bc4-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="61bc4-130">Os números de mensagem no quinto intervalo (maior que 0xFFFF) são reservados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="61bc4-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="61bc4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61bc4-131">Requirements</span></span>



| <span data-ttu-id="61bc4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="61bc4-132">Requirement</span></span> | <span data-ttu-id="61bc4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="61bc4-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61bc4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61bc4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="61bc4-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61bc4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="61bc4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61bc4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="61bc4-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61bc4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="61bc4-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61bc4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="61bc4-139"><dt>OLECTL. h</dt></span><span class="sxs-lookup"><span data-stu-id="61bc4-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61bc4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="61bc4-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="61bc4-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="61bc4-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61bc4-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="61bc4-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="61bc4-143">**aplicativo do WM \_**</span><span class="sxs-lookup"><span data-stu-id="61bc4-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="61bc4-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="61bc4-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61bc4-145">Mensagens e filas de mensagens</span><span class="sxs-lookup"><span data-stu-id="61bc4-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

