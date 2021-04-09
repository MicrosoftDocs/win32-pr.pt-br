---
title: Controle de Up-Down
description: Esta seção contém informações sobre os elementos de programação usados com controles de cima para baixo.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005355"
---
# <a name="up-down-control"></a><span data-ttu-id="a069e-103">Controle de Up-Down</span><span class="sxs-lookup"><span data-stu-id="a069e-103">Up-Down Control</span></span>

<span data-ttu-id="a069e-104">Esta seção contém informações sobre os elementos de programação usados com controles de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="a069e-105">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="a069e-105">Overviews</span></span>



| <span data-ttu-id="a069e-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-106">Topic</span></span>                                    | <span data-ttu-id="a069e-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-108">Controles de cima para baixo</span><span class="sxs-lookup"><span data-stu-id="a069e-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="a069e-109">Um controle de cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle complementar (chamado de janela Buddy).</span><span class="sxs-lookup"><span data-stu-id="a069e-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="a069e-110">Funções</span><span class="sxs-lookup"><span data-stu-id="a069e-110">Functions</span></span>



| <span data-ttu-id="a069e-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-111">Topic</span></span>                                              | <span data-ttu-id="a069e-112">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-113">**CreateUpDownControl**</span><span class="sxs-lookup"><span data-stu-id="a069e-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="a069e-114">Cria um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-114">Creates an up-down control.</span></span> <span data-ttu-id="a069e-115">Observação: essa função está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="a069e-115">Note: This function is obsolete.</span></span> <span data-ttu-id="a069e-116">É uma função de 16 bits e não pode manipular valores de 32 bits para intervalo e posição.</span><span class="sxs-lookup"><span data-stu-id="a069e-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="a069e-117">Mensagens</span><span class="sxs-lookup"><span data-stu-id="a069e-117">Messages</span></span>



| <span data-ttu-id="a069e-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-118">Topic</span></span>                                                 | <span data-ttu-id="a069e-119">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-120">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="a069e-121">Recupera informações de aceleração para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="a069e-122">**UDM \_ GETbase**</span><span class="sxs-lookup"><span data-stu-id="a069e-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="a069e-123">Recupera a base da Radix atual (ou seja, a base 10 ou 16) para um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="a069e-124">**UDM \_ GETbuddy**</span><span class="sxs-lookup"><span data-stu-id="a069e-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="a069e-125">Recupera o identificador para a janela atual do Buddy.</span><span class="sxs-lookup"><span data-stu-id="a069e-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="a069e-126">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="a069e-127">Recupera a posição atual de um controle de cima para baixo com precisão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a069e-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="a069e-128">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="a069e-129">Retorna a posição de 32 bits de um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="a069e-130">**GetRange do UDM \_**</span><span class="sxs-lookup"><span data-stu-id="a069e-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="a069e-131">Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="a069e-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="a069e-133">Recupera o intervalo de 32 bits de um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="a069e-134">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="a069e-135">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="a069e-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="a069e-136">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="a069e-137">Define a aceleração para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="a069e-138">**UDM \_ SETbase**</span><span class="sxs-lookup"><span data-stu-id="a069e-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="a069e-139">Define a base do Radix para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="a069e-140">O valor base determina se a janela buddy exibe números em dígitos decimais ou hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a069e-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="a069e-141">Os números hexadecimais são sempre não assinados e números decimais são assinados.</span><span class="sxs-lookup"><span data-stu-id="a069e-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="a069e-142">**UDM \_ SETbuddy**</span><span class="sxs-lookup"><span data-stu-id="a069e-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="a069e-143">Define a janela Buddy para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="a069e-144">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="a069e-145">Define a posição atual para um controle de cima para baixo com precisão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a069e-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="a069e-146">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="a069e-147">Define a posição de um controle de cima para baixo com precisão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a069e-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="a069e-148">**SETRANGE de UDM \_**</span><span class="sxs-lookup"><span data-stu-id="a069e-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="a069e-149">Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="a069e-150">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="a069e-151">Define o intervalo de 32 bits de um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="a069e-152">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="a069e-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="a069e-153">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="a069e-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="a069e-154">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="a069e-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="a069e-155">Notificações</span><span class="sxs-lookup"><span data-stu-id="a069e-155">Notifications</span></span>



| <span data-ttu-id="a069e-156">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-156">Topic</span></span>                                                            | <span data-ttu-id="a069e-157">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-158">NM \_ RELEASEDCAPTURE (up-down)</span><span class="sxs-lookup"><span data-stu-id="a069e-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="a069e-159">Notifica uma janela pai do controle up que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="a069e-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="a069e-160">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a069e-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="a069e-161">UDN \_ DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="a069e-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="a069e-162">Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="a069e-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="a069e-163">Isso acontece quando o usuário solicita uma alteração no valor pressionando a seta para cima ou para baixo do controle.</span><span class="sxs-lookup"><span data-stu-id="a069e-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="a069e-164">A mensagem [UDN \_ DELTAPOS](udn-deltapos.md) é enviada na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a069e-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="a069e-165">Estruturas</span><span class="sxs-lookup"><span data-stu-id="a069e-165">Structures</span></span>



| <span data-ttu-id="a069e-166">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-166">Topic</span></span>                        | <span data-ttu-id="a069e-167">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-168">**NMUPDOWN**</span><span class="sxs-lookup"><span data-stu-id="a069e-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="a069e-169">Contém informações específicas para as mensagens de notificação de controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="a069e-170">É idêntico a e substitui a estrutura **do \_ nm** .</span><span class="sxs-lookup"><span data-stu-id="a069e-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="a069e-171">**UDACCEL**</span><span class="sxs-lookup"><span data-stu-id="a069e-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="a069e-172">Contém informações de aceleração para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="a069e-173">Constantes</span><span class="sxs-lookup"><span data-stu-id="a069e-173">Constants</span></span>



| <span data-ttu-id="a069e-174">Tópico</span><span class="sxs-lookup"><span data-stu-id="a069e-174">Topic</span></span>                                                | <span data-ttu-id="a069e-175">Sumário</span><span class="sxs-lookup"><span data-stu-id="a069e-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="a069e-176">Estilos de controle de cima para baixo</span><span class="sxs-lookup"><span data-stu-id="a069e-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="a069e-177">Esta seção lista os estilos usados ao criar controles de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="a069e-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





