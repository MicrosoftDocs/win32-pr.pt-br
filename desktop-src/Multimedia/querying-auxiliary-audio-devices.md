---
title: Consultando dispositivos de áudio auxiliares
description: Consultando dispositivos de áudio auxiliares
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- áudio de onda, consultando dispositivos de áudio auxiliares
- áudio auxiliar, consultando dispositivos
- interface de áudio auxiliar
- dispositivos de áudio auxiliares, consultando
- consultando dispositivos de áudio auxiliares
- áudio auxiliar, interface
- áudio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007429"
---
# <a name="querying-auxiliary-audio-devices"></a><span data-ttu-id="4ef15-110">Consultando dispositivos de áudio auxiliares</span><span class="sxs-lookup"><span data-stu-id="4ef15-110">Querying Auxiliary Audio Devices</span></span>

<span data-ttu-id="4ef15-111">Nem todos os sistemas de multimídia têm suporte de áudio auxiliar.</span><span class="sxs-lookup"><span data-stu-id="4ef15-111">Not all multimedia systems have auxiliary audio support.</span></span> <span data-ttu-id="4ef15-112">Você pode usar a função [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) para determinar o número de dispositivos auxiliares controláveis presentes em um sistema.</span><span class="sxs-lookup"><span data-stu-id="4ef15-112">You can use the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) function to determine the number of controllable auxiliary devices present in a system.</span></span>

<span data-ttu-id="4ef15-113">Para obter informações sobre um dispositivo de áudio auxiliar específico, use a função [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="4ef15-113">To get information about a particular auxiliary audio device, use the [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) function.</span></span> <span data-ttu-id="4ef15-114">Essa função preenche uma estrutura [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) com informações sobre os recursos de um dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4ef15-114">This function fills an [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="4ef15-115">Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ef15-115">This information includes the manufacturer and product identifiers, a product name for the device, and the device-driver version number.</span></span>

 

 