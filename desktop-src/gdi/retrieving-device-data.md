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
# <a name="retrieving-device-data"></a>Recuperando dados do dispositivo

Os aplicativos podem usar as seguintes funções para recuperar dados de dispositivo usando um contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera dados gerais do dispositivo para os seguintes dispositivos:

-   Telas de varredura
-   Impressoras matricial
-   Impressoras jato de tinta
-   Impressoras a laser
-   Plotagens de vetor
-   Câmeras rasterizadas

Os dados incluem os recursos com suporte do dispositivo, incluindo a resolução de dispositivo (para vídeos), o formato de cor (para telas de vídeo e impressoras coloridas), o número de objetos gráficos, recursos de rasterização, desenho de curva, desenho de linha, desenho de polígono e desenho de texto. Um aplicativo recupera esses dados fornecendo um identificador que identifica o contexto do dispositivo apropriado, bem como um índice especificando o tipo de dados que a função deve recuperar.

A função [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera dados específicos para impressoras, incluindo o número de compartimentos de papel disponíveis, os recursos duplex da impressora, as resoluções com suporte na impressora, o tamanho máximo e mínimo de papel com suporte e assim por diante. Um aplicativo recupera esses dados fornecendo cadeias de caracteres especificando um dispositivo de impressora e uma porta, bem como um índice especificando o tipo de dados que a função deve recuperar.

 

 
