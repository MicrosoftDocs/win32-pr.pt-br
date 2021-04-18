---
description: Os especificadores de tipo de dispositivo WIA (aquisição de imagem do Windows) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Especificadores de tipo de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793866"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="17dd0-103">Especificadores de tipo de dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="17dd0-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="17dd0-104">Os especificadores de tipo de dispositivo WIA (aquisição de imagem do Windows) são constantes que indicam o tipo de dispositivo anexado ao computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="17dd0-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="17dd0-105">Use a \_ macro obter \_ tipo STIDEVICE para obter esses valores da Propriedade do tipo de dispositivo WIA.</span><span class="sxs-lookup"><span data-stu-id="17dd0-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="17dd0-106">Estes são especificadores de tipo de dispositivo WIA válidos:</span><span class="sxs-lookup"><span data-stu-id="17dd0-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="17dd0-107">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="17dd0-107">Device Type</span></span>                 | <span data-ttu-id="17dd0-108">Significado</span><span class="sxs-lookup"><span data-stu-id="17dd0-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17dd0-109">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="17dd0-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="17dd0-110">Dispositivo WIA genérico.</span><span class="sxs-lookup"><span data-stu-id="17dd0-110">Generic WIA device.</span></span> <span data-ttu-id="17dd0-111">Durante as enumerações de dispositivo, essa constante é usada para enumerar todos os dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="17dd0-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="17dd0-112">StiDeviceTypeDigitalCamera</span><span class="sxs-lookup"><span data-stu-id="17dd0-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="17dd0-113">O dispositivo é uma câmera.</span><span class="sxs-lookup"><span data-stu-id="17dd0-113">The device is a camera.</span></span> <span data-ttu-id="17dd0-114">*Não há suporte para este especificador por* Windows Vista *e posterior.*</span><span class="sxs-lookup"><span data-stu-id="17dd0-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="17dd0-115">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="17dd0-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="17dd0-116">O dispositivo é um scanner.</span><span class="sxs-lookup"><span data-stu-id="17dd0-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="17dd0-117">StiDeviceTypeStreamingVideo</span><span class="sxs-lookup"><span data-stu-id="17dd0-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="17dd0-118">O dispositivo contém vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="17dd0-118">The device contains streaming video.</span></span> <span data-ttu-id="17dd0-119">*Não há suporte para este especificador por* Windows Server 2003 *,* Windows Vista *ou posterior.*</span><span class="sxs-lookup"><span data-stu-id="17dd0-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



