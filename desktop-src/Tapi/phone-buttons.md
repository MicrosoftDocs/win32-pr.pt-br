---
description: A TAPI modela os botões e as lâmpadas dos telefones como os pares de luzes de botão.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Botões de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661784"
---
# <a name="phone-buttons"></a><span data-ttu-id="a4ceb-103">Botões de telefone</span><span class="sxs-lookup"><span data-stu-id="a4ceb-103">Phone Buttons</span></span>

<span data-ttu-id="a4ceb-104">A TAPI modela os botões e as lâmpadas de um telefone como pares de luzes de botão.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="a4ceb-105">Um botão sem nenhuma lâmpada ao lado dele ou uma lâmpada sem nenhum botão é especificado usando um indicador "fictício" para a lâmpada ou o botão ausente.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="a4ceb-106">Um botão com várias lâmpadas é modelado usando vários pares de botões de lâmpada.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="a4ceb-107">As informações associadas a um botão de telefone podem ser definidas e recuperadas.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="a4ceb-108">Quando um botão é pressionado, uma mensagem de [**\_ botão de telefone**](phone-button.md) é enviada para a função do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="a4ceb-109">Os parâmetros dessa mensagem são um identificador para o dispositivo de telefone e o identificador de lâmpada de botão do botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="a4ceb-110">Os botões de teclado ' 0 ' a ' 9 ', ' \* ' e ' \# ' são atribuídos ao botão fixo – identificadores de lâmpada de 0 a 11.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="a4ceb-111">As funções associadas aos botões são [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que define as informações associadas a um botão em um dispositivo de telefone e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que retorna informações associadas a um botão em um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="a4ceb-112">A \_ mensagem do botão telefone é enviada a um aplicativo quando um botão no telefone é pressionado.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="a4ceb-113">As informações associadas a um botão não têm nenhum significado semântico no que diz respeito à TAPI.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="a4ceb-114">Ele é útil para aplicativos específicos do dispositivo que entendem o significado dessas informações para um determinado dispositivo de telefone, ou para exibição para o usuário, como a ajuda online.</span><span class="sxs-lookup"><span data-stu-id="a4ceb-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



