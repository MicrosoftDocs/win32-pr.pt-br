---
description: Os modelos de telefonia da Microsoft são botões e lâmpadas de telefones como pares de luzes de botão.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Botões (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757001"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="c97ff-103">Botões (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="c97ff-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="c97ff-104">A telefonia da Microsoft modela os botões e as lâmpadas de um telefone como pares de luzes de botão.</span><span class="sxs-lookup"><span data-stu-id="c97ff-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="c97ff-105">Um botão sem nenhuma lâmpada ao lado ou uma lâmpada sem nenhum botão é especificado usando um indicador fictício para a lâmpada ou o botão ausente.</span><span class="sxs-lookup"><span data-stu-id="c97ff-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="c97ff-106">Um botão com várias lâmpadas é modelado usando vários pares de botões de lâmpada.</span><span class="sxs-lookup"><span data-stu-id="c97ff-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="c97ff-107">As informações associadas a um botão de telefone podem ser definidas e recuperadas.</span><span class="sxs-lookup"><span data-stu-id="c97ff-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="c97ff-108">Quando um botão é pressionado, o provedor de serviços envia uma mensagem de [**\_ botão de telefone**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) para a função de retorno de chamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="c97ff-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="c97ff-109">Os parâmetros dessa mensagem são um identificador para o dispositivo de telefone e o identificador de botão/lâmpada do botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="c97ff-110">O botão do teclado ' 0 ' por meio de ' 9 ', ' \* ' e ' \# ' recebe identificadores de botão/lâmpada fixos de 0 a 11.</span><span class="sxs-lookup"><span data-stu-id="c97ff-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="c97ff-111">A função [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) define as informações associadas a um botão em um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="c97ff-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="c97ff-112">[**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) retorna informações associadas a um botão em um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="c97ff-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="c97ff-113">O provedor de serviços envia uma \_ mensagem de botão de telefone para a função de retorno de chamada TAPI quando um botão no telefone é pressionado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="c97ff-114">As informações associadas a um botão não têm nenhum significado semântico no que diz respeito ao TSPI.</span><span class="sxs-lookup"><span data-stu-id="c97ff-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="c97ff-115">Ele é útil para aplicativos específicos do dispositivo que interpretam essas informações para um determinado dispositivo de telefone ou para exibição para o usuário, como no sistema de ajuda de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
