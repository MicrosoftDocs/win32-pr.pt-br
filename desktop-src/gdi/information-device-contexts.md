---
description: O controlador de domínio de informações é usado para recuperar dados de dispositivo padrão.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contextos de dispositivo de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502413"
---
# <a name="information-device-contexts"></a><span data-ttu-id="723db-103">Contextos de dispositivo de informações</span><span class="sxs-lookup"><span data-stu-id="723db-103">Information Device Contexts</span></span>

<span data-ttu-id="723db-104">O controlador de domínio de informações é usado para recuperar dados de dispositivo padrão.</span><span class="sxs-lookup"><span data-stu-id="723db-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="723db-105">Por exemplo, um aplicativo pode chamar a função [**createy**](/windows/desktop/api/Wingdi/nf-wingdi-createica) para criar um controlador de domínio de informações para um modelo específico de impressora e, em seguida, chamar as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) para recuperar os atributos padrão da caneta ou do pincel.</span><span class="sxs-lookup"><span data-stu-id="723db-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="723db-106">Como o sistema pode recuperar informações do dispositivo sem criar as estruturas normalmente associadas a outros tipos de contextos de dispositivo, um controlador de domínio de informações envolve muito menos sobrecarga e é criado significativamente mais rápido do que qualquer um dos outros tipos.</span><span class="sxs-lookup"><span data-stu-id="723db-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="723db-107">Depois que um aplicativo termina de recuperar dados usando um controlador de domínio de informações, ele deve chamar a função [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="723db-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



