---
title: Alterando a posição atual
description: Alterando a posição atual
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366024"
---
# <a name="changing-the-current-position"></a><span data-ttu-id="55d61-104">Alterando a posição atual</span><span class="sxs-lookup"><span data-stu-id="55d61-104">Changing the Current Position</span></span>

<span data-ttu-id="55d61-105">Para alterar a posição atual em um elemento de dispositivo, use a mensagem de comando [**MCI \_ Seek**](mci-seek.md) junto com o MCI \_ para sinalizar e a estrutura de [**\_ \_ parâmetros de busca do MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="55d61-105">To change the current position in a device element, use the [**MCI\_SEEK**](mci-seek.md) command message along with the MCI\_TO flag and the [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="55d61-106">Se você usar o membro **dwTo** para especificar uma posição de busca com o MCI \_ Seek, deverá consultar o formato de hora e defini-lo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="55d61-106">If you use the **dwTo** member to specify a seek position with MCI\_SEEK, you should query the time format and set it, if necessary.</span></span>

<span data-ttu-id="55d61-107">Além de especificar uma posição com o membro **dwTo** , você pode especificar o MCI \_ Seek \_ para \_ Iniciar ou MCI \_ buscar \_ até sinalizadores de \_ fim para o parâmetro *dwParam1* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para localizar as posições inicial e final do elemento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55d61-107">In addition to specifying a position with the **dwTo** member, you can specify the MCI\_SEEK\_TO\_START or MCI\_SEEK\_TO\_END flags for the *dwParam1* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to find the starting and ending positions of the device element.</span></span> <span data-ttu-id="55d61-108">Se você usar um desses sinalizadores, não especifique o MCI \_ a ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="55d61-108">If you use one of these flags, don't specify the MCI\_TO flag.</span></span>

 

 