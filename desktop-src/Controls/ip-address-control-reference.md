---
title: Controle de endereço IP
description: Esta seção contém informações sobre os elementos de programação usados com controles de endereço IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453553"
---
# <a name="ip-address-control"></a><span data-ttu-id="f15fc-103">Controle de endereço IP</span><span class="sxs-lookup"><span data-stu-id="f15fc-103">IP Address Control</span></span>

<span data-ttu-id="f15fc-104">Esta seção contém informações sobre os elementos de programação usados com controles de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="f15fc-105">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="f15fc-105">Overviews</span></span>



| <span data-ttu-id="f15fc-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="f15fc-106">Topic</span></span>                                          | <span data-ttu-id="f15fc-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="f15fc-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15fc-108">Controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="f15fc-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="f15fc-109">Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido.</span><span class="sxs-lookup"><span data-stu-id="f15fc-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="f15fc-110">Macros</span><span class="sxs-lookup"><span data-stu-id="f15fc-110">Macros</span></span>



| <span data-ttu-id="f15fc-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="f15fc-111">Topic</span></span>                                         | <span data-ttu-id="f15fc-112">Sumário</span><span class="sxs-lookup"><span data-stu-id="f15fc-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15fc-113">**PRIMEIRO \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="f15fc-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="f15fc-114">Extrai o valor do campo 0 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f15fc-115">**QUARTO \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="f15fc-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="f15fc-116">Extrai o valor do campo 3 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f15fc-117">**MAKEIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f15fc-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="f15fc-118">Empacota quatro valores de byte em um único LPARAM adequado para uso com a mensagem [**IPM \_ SetAddress**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="f15fc-119">**MAKEIPRANGE**</span><span class="sxs-lookup"><span data-stu-id="f15fc-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="f15fc-120">Compacta dois valores de byte em um único LPARAM adequado para uso com a mensagem [**IPM \_ SETRANGE**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="f15fc-121">**SEGUNDO \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="f15fc-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="f15fc-122">Extrai o valor do campo 1 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f15fc-123">**TERCEIRO \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="f15fc-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="f15fc-124">Extrai o valor do campo 2 de um endereço IP empacotado recuperado com a mensagem [**IPM \_ GetAddress**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="f15fc-125">Mensagens</span><span class="sxs-lookup"><span data-stu-id="f15fc-125">Messages</span></span>



| <span data-ttu-id="f15fc-126">Tópico</span><span class="sxs-lookup"><span data-stu-id="f15fc-126">Topic</span></span>                                         | <span data-ttu-id="f15fc-127">Sumário</span><span class="sxs-lookup"><span data-stu-id="f15fc-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15fc-128">**\_CLEARADDRESS IPM**</span><span class="sxs-lookup"><span data-stu-id="f15fc-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="f15fc-129">Limpa o conteúdo do controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="f15fc-130">**\ \_ endereço IPM**</span><span class="sxs-lookup"><span data-stu-id="f15fc-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="f15fc-131">Obtém os valores de endereço para todos os quatro campos no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="f15fc-132">**IPM \_ ISblank**</span><span class="sxs-lookup"><span data-stu-id="f15fc-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="f15fc-133">Determina se todos os campos no controle de endereço IP estão em branco.</span><span class="sxs-lookup"><span data-stu-id="f15fc-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="f15fc-134">**de \_ IPM**</span><span class="sxs-lookup"><span data-stu-id="f15fc-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="f15fc-135">Define os valores de endereço para todos os quatro campos no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="f15fc-136">**IPM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="f15fc-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="f15fc-137">Define o foco do teclado para o campo especificado no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="f15fc-138">Todo o texto nesse campo será selecionado.</span><span class="sxs-lookup"><span data-stu-id="f15fc-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="f15fc-139">**IPM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="f15fc-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="f15fc-140">Define o intervalo válido para o campo especificado no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f15fc-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="f15fc-141">Notificações</span><span class="sxs-lookup"><span data-stu-id="f15fc-141">Notifications</span></span>



| <span data-ttu-id="f15fc-142">Tópico</span><span class="sxs-lookup"><span data-stu-id="f15fc-142">Topic</span></span>                                     | <span data-ttu-id="f15fc-143">Sumário</span><span class="sxs-lookup"><span data-stu-id="f15fc-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15fc-144">\_campo IPN</span><span class="sxs-lookup"><span data-stu-id="f15fc-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="f15fc-145">Enviado quando o usuário altera um campo no controle ou move de um campo para outro.</span><span class="sxs-lookup"><span data-stu-id="f15fc-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="f15fc-146">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="f15fc-147">Estruturas</span><span class="sxs-lookup"><span data-stu-id="f15fc-147">Structures</span></span>



| <span data-ttu-id="f15fc-148">Tópico</span><span class="sxs-lookup"><span data-stu-id="f15fc-148">Topic</span></span>                              | <span data-ttu-id="f15fc-149">Sumário</span><span class="sxs-lookup"><span data-stu-id="f15fc-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15fc-150">**NMIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f15fc-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="f15fc-151">Contém informações para o código de notificação [ \_ FieldChanged IPN](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="f15fc-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 





