---
description: Um único telefone pode ser capaz de tocar com diferentes modos de toque.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921692"
---
# <a name="ring"></a><span data-ttu-id="b5539-103">Anel</span><span class="sxs-lookup"><span data-stu-id="b5539-103">Ring</span></span>

<span data-ttu-id="b5539-104">Um único telefone pode ser capaz de tocar com diferentes modos de toque.</span><span class="sxs-lookup"><span data-stu-id="b5539-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="b5539-105">Considerando a ampla variedade de modos de toque disponíveis, os modos de toque são identificados por meio de seu número de modo de toque.</span><span class="sxs-lookup"><span data-stu-id="b5539-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="b5539-106">Um número de modo de anel varia de zero para o número de modos de anel disponíveis menos um.</span><span class="sxs-lookup"><span data-stu-id="b5539-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="b5539-107">As funções que um aplicativo usaria para controlar os modos de toque de um dispositivo de telefone são [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que toca um dispositivo de telefone aberto de acordo com um determinado modo de toque e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que retorna o modo de toque atual de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="b5539-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="b5539-108">Quando o modo de anel de um dispositivo de telefone é alterado, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b5539-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="b5539-109">Os parâmetros dessa mensagem fornecem uma indicação da alteração.</span><span class="sxs-lookup"><span data-stu-id="b5539-109">Parameters to this message provide an indication of the change.</span></span>

 

 



