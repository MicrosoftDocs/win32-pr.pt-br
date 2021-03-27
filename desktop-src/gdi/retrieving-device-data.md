---
description: 'Os aplicativos podem usar as seguintes funções para recuperar dados de dispositivo usando um contexto de dispositivo: GetDeviceCaps e DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recuperando dados do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967589"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="af0f2-103">Recuperando dados do dispositivo</span><span class="sxs-lookup"><span data-stu-id="af0f2-103">Retrieving Device Data</span></span>

<span data-ttu-id="af0f2-104">Os aplicativos podem usar as seguintes funções para recuperar dados de dispositivo usando um contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span><span class="sxs-lookup"><span data-stu-id="af0f2-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="af0f2-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera dados gerais do dispositivo para os seguintes dispositivos:</span><span class="sxs-lookup"><span data-stu-id="af0f2-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="af0f2-106">Telas de varredura</span><span class="sxs-lookup"><span data-stu-id="af0f2-106">Raster displays</span></span>
-   <span data-ttu-id="af0f2-107">Impressoras matricial</span><span class="sxs-lookup"><span data-stu-id="af0f2-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="af0f2-108">Impressoras jato de tinta</span><span class="sxs-lookup"><span data-stu-id="af0f2-108">Ink-jet printers</span></span>
-   <span data-ttu-id="af0f2-109">Impressoras a laser</span><span class="sxs-lookup"><span data-stu-id="af0f2-109">Laser printers</span></span>
-   <span data-ttu-id="af0f2-110">Plotagens de vetor</span><span class="sxs-lookup"><span data-stu-id="af0f2-110">Vector plotters</span></span>
-   <span data-ttu-id="af0f2-111">Câmeras rasterizadas</span><span class="sxs-lookup"><span data-stu-id="af0f2-111">Raster cameras</span></span>

<span data-ttu-id="af0f2-112">Os dados incluem os recursos com suporte do dispositivo, incluindo a resolução de dispositivo (para vídeos), o formato de cor (para telas de vídeo e impressoras coloridas), o número de objetos gráficos, recursos de rasterização, desenho de curva, desenho de linha, desenho de polígono e desenho de texto.</span><span class="sxs-lookup"><span data-stu-id="af0f2-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="af0f2-113">Um aplicativo recupera esses dados fornecendo um identificador que identifica o contexto do dispositivo apropriado, bem como um índice especificando o tipo de dados que a função deve recuperar.</span><span class="sxs-lookup"><span data-stu-id="af0f2-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="af0f2-114">A função [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera dados específicos para impressoras, incluindo o número de compartimentos de papel disponíveis, os recursos duplex da impressora, as resoluções com suporte na impressora, o tamanho máximo e mínimo de papel com suporte e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="af0f2-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="af0f2-115">Um aplicativo recupera esses dados fornecendo cadeias de caracteres especificando um dispositivo de impressora e uma porta, bem como um índice especificando o tipo de dados que a função deve recuperar.</span><span class="sxs-lookup"><span data-stu-id="af0f2-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
