---
title: Sobre controles de endereço IP
description: Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6859bd31250d30bcf26d0c5fde37afeca8cc81bd
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424226"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="afe30-103">Sobre controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="afe30-103">About IP Address Controls</span></span>

<span data-ttu-id="afe30-104">Um controle de endereço IP (Internet Protocol) permite que o usuário insira um endereço IP em um formato facilmente compreendido.</span><span class="sxs-lookup"><span data-stu-id="afe30-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="afe30-105">Esse controle também permite que o aplicativo obtenha o endereço em formato numérico em vez de em formato de texto.</span><span class="sxs-lookup"><span data-stu-id="afe30-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="afe30-106">Sobre controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="afe30-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="afe30-107">Criando um controle de endereço IP</span><span class="sxs-lookup"><span data-stu-id="afe30-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="afe30-108">Um controle de endereço IP é um controle de edição?</span><span class="sxs-lookup"><span data-stu-id="afe30-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="afe30-109">Sobre controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="afe30-109">About IP Address Controls</span></span>

<span data-ttu-id="afe30-110">O Windows Internet Explorer versão 4,0 apresenta o controle de endereço IP, um novo controle semelhante a um controle de edição que permite ao usuário inserir um endereço numérico no formato de protocolo IP.</span><span class="sxs-lookup"><span data-stu-id="afe30-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="afe30-111">Esse formato consiste em campos de 4 3 dígitos.</span><span class="sxs-lookup"><span data-stu-id="afe30-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="afe30-112">Cada campo é tratado individualmente; os números de campo são baseados em zero e passam da esquerda para a direita, conforme mostrado nesta figura.</span><span class="sxs-lookup"><span data-stu-id="afe30-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![diagrama mostrando valores em cada um dos quatro campos de um controle de endereço IP](images/ipa-scrn.png)

<span data-ttu-id="afe30-114">O controle permite que apenas texto numérico seja inserido em cada um dos campos.</span><span class="sxs-lookup"><span data-stu-id="afe30-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="afe30-115">Depois que três dígitos forem inseridos em um determinado campo, o foco do teclado será movido automaticamente para o próximo campo.</span><span class="sxs-lookup"><span data-stu-id="afe30-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="afe30-116">Se o preenchimento do campo inteiro não for exigido pelo aplicativo, o usuário poderá inserir menos de três dígitos.</span><span class="sxs-lookup"><span data-stu-id="afe30-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="afe30-117">Por exemplo, se o campo deve conter apenas o número vinte e um, digitando "21" e pressionar a tecla, o usuário será levado para o próximo campo.</span><span class="sxs-lookup"><span data-stu-id="afe30-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="afe30-118">O intervalo padrão para cada campo é de 0 a 255, mas o aplicativo pode definir o intervalo para quaisquer valores entre esses limites com a mensagem [**IPM \_ SETRANGE**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="afe30-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="afe30-119">O controle de endereço IP é implementado na versão 4,71 e posterior do Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="afe30-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="afe30-120">Criando um controle de endereço IP</span><span class="sxs-lookup"><span data-stu-id="afe30-120">Creating an IP Address Control</span></span>

<span data-ttu-id="afe30-121">Antes de criar um controle de endereço IP, chame [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o sinalizador **ICC \_ INTERNET \_ CLASSES** definido no membro **dwICC** da estrutura [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)</span><span class="sxs-lookup"><span data-stu-id="afe30-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="afe30-122">Use a [**função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="afe30-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="afe30-123">O nome da classe para o controle [**é WC \_ IPADDRESS,**](common-control-window-classes.md)que é definido em Commctrl.h.</span><span class="sxs-lookup"><span data-stu-id="afe30-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="afe30-124">Não existem estilos específicos do controle de endereço IP; no entanto, como esse é um controle filho, use o [**estilo FILHO do WS \_**](/windows/desktop/winmsg/window-styles) como um mínimo.</span><span class="sxs-lookup"><span data-stu-id="afe30-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="afe30-125">Um controle de endereço IP é um controle de edição?</span><span class="sxs-lookup"><span data-stu-id="afe30-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="afe30-126">Um controle de endereço IP não é um controle de edição e não responderá a mensagens \_ EM.</span><span class="sxs-lookup"><span data-stu-id="afe30-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="afe30-127">No entanto, ele enviará à janela do proprietário as seguintes notificações de controle de edição por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="afe30-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="afe30-128">Observe que o controle de endereço IP também enviará notificações de IPN privado \_ por meio da mensagem WM [**\_ NOTIFY.**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="afe30-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|     <span data-ttu-id="afe30-129">Notificação</span><span class="sxs-lookup"><span data-stu-id="afe30-129">Notification</span></span>                              |     <span data-ttu-id="afe30-130">Motivo da notificação</span><span class="sxs-lookup"><span data-stu-id="afe30-130">Reason for notification</span></span>                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afe30-131">EN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="afe30-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="afe30-132">Enviado quando o controle de endereço IP obtém o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="afe30-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="afe30-133">EN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="afe30-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="afe30-134">Enviado quando o controle de endereço IP perde o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="afe30-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="afe30-135">EN \_ CHANGE</span><span class="sxs-lookup"><span data-stu-id="afe30-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="afe30-136">Enviado quando qualquer campo no controle de endereço IP muda.</span><span class="sxs-lookup"><span data-stu-id="afe30-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="afe30-137">Como a [ \_ notificação EN CHANGE](en-change.md) de um controle de edição padrão, essa notificação é recebida após a atualização da tela.</span><span class="sxs-lookup"><span data-stu-id="afe30-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 