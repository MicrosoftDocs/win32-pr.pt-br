---
description: 'Os aplicativos podem usar as seguintes funções para recuperar dados do dispositivo usando um contexto de dispositivo: GetDeviceCaps e DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recuperando dados do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717986"
---
# <a name="retrieving-device-data"></a>Recuperando dados do dispositivo

Os aplicativos podem usar as seguintes funções para recuperar dados do dispositivo usando um contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities.**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera dados gerais do dispositivo para os seguintes dispositivos:

-   Exibições de raster
-   Impressoras dot-matrix
-   Impressoras ink-jet
-   Impressoras de raios
-   Plotador de vetor
-   Câmeras de raster

Os dados incluem os recursos com suporte do dispositivo, incluindo resolução de dispositivo (para exibições de vídeo), formato de cor (para exibições de vídeo e impressoras de cores), número de objetos gráficos, recursos de raster, desenho de curva, desenho de linha, desenho de polígono e desenho de texto. Um aplicativo recupera esses dados fornecendo um identificador que identifica o contexto do dispositivo apropriado, bem como um índice que especifica o tipo de dados que a função deve recuperar.

A [**função DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera dados específicos para impressoras, incluindo o número de compartimentos de papel disponíveis, os recursos duplex da impressora, as resoluções com suporte pela impressora, o tamanho máximo e mínimo de papel com suporte e assim por diante. Um aplicativo recupera esses dados fornecendo cadeias de caracteres especificando um dispositivo de impressora e uma porta, bem como um índice que especifica o tipo de dados que a função deve recuperar.

 

 
