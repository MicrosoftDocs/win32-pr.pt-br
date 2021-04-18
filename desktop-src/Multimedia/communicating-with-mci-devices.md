---
title: Comunicando-se com dispositivos MCI
description: Comunicando-se com dispositivos MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Macro MCIWndSendString
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752627"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="33674-105">Comunicando-se com dispositivos MCI</span><span class="sxs-lookup"><span data-stu-id="33674-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="33674-106">O driver de cada dispositivo MCI mantém uma lista de suas configurações e recursos atuais, de modo que ele pode emitir uma resposta precisa quando é consultado para obter informações.</span><span class="sxs-lookup"><span data-stu-id="33674-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="33674-107">Quando você quiser se comunicar com um dispositivo MCI, poderá usar macros e funções do MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="33674-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="33674-108">Muitos dos comandos e consultas MCI mais comuns são definidos como macros.</span><span class="sxs-lookup"><span data-stu-id="33674-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="33674-109">No entanto, se a tarefa que você deseja executar não estiver disponível como uma função ou macro, você poderá enviar comandos MCI diretamente para o driver de dispositivo usando a macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) ou o formulário de mensagem ou a forma de cadeia de caracteres dos comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="33674-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="33674-110">O uso da macro **MCIWndSendString** é equivalente ao uso da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="33674-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="33674-111">Os parâmetros de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) incluem apenas o identificador de janela e a forma de cadeia de caracteres do comando.</span><span class="sxs-lookup"><span data-stu-id="33674-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="33674-112">Para recuperar as informações retornadas por um comando de cadeia de caracteres, use a macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="33674-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="33674-113">Para obter mais informações sobre o MCI, consulte [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="33674-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="33674-114">Você deve excluir o alias do dispositivo do comando MCI ao usar o **MCIWndSendString**.</span><span class="sxs-lookup"><span data-stu-id="33674-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="33674-115">A biblioteca MCIWnd adiciona esse alias quando envia o comando para o dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="33674-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 