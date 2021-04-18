---
description: Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes que ele possa acessar funções nesse telefone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Abrindo e fechando dispositivos de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810128"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="e3c25-103">Abrindo e fechando dispositivos de telefone</span><span class="sxs-lookup"><span data-stu-id="e3c25-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="e3c25-104">Depois de determinar os recursos de um dispositivo de telefone, um aplicativo deve abrir o dispositivo antes que ele possa acessar funções nesse telefone.</span><span class="sxs-lookup"><span data-stu-id="e3c25-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="e3c25-105">Depois que um dispositivo de telefone é aberto com êxito, o aplicativo retorna um identificador que representa o telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="e3c25-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="e3c25-106">Um dispositivo de telefone pode ser aberto em modos diferentes, fornecendo, assim, uma maneira estruturada de compartilhar um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="e3c25-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="e3c25-107">A função [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre o dispositivo de telefone especificado para conceder ao aplicativo acesso a funções no telefone.</span><span class="sxs-lookup"><span data-stu-id="e3c25-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="e3c25-108">Um dispositivo de telefone é identificado como **phoneOpen** por meio de seu identificador de dispositivo, que é passado como o parâmetro *dwDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="e3c25-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 



