---
title: Descobrindo recursos de formato de dispositivo
description: Descobrindo recursos de formato de dispositivo
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Gerenciador de Dispositivos de mídia, recursos do dispositivo
- Gerenciador de Dispositivos, recursos do dispositivo
- Guia de programação, recursos do dispositivo
- aplicativos de desktop, recursos de dispositivo
- criação de aplicativos de Gerenciador de Dispositivos de mídia Windows, recursos de dispositivo
- gravando arquivos em dispositivos, recursos do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4fc32c0980a1022f7affb225918ccf0d49e5d14c5bb7310e70e7aa4f83a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585142"
---
# <a name="discovering-device-format-capabilities"></a>Descobrindo recursos de formato de dispositivo

Seu aplicativo pode tentar determinar os recursos de reprodução de um dispositivo antes de enviar um arquivo para ele. Se um dispositivo não puder manipular o formato de um arquivo que você deseja enviar, seu aplicativo poderá tentar transcodificar o arquivo em um formato que o dispositivo possa usar ou notificar o usuário de que o dispositivo não pode dar suporte ao arquivo solicitado.

Observe que alguns dispositivos, como dispositivos de classe de armazenamento em massa, podem servir apenas como mídia de armazenamento removível sem recursos de reprodução. Nesse caso, seria inapropriado que seu aplicativo transcodifique um arquivo antes de enviá-lo para o dispositivo.

Embora o método [**IWMDMDevice:: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) permita que um dispositivo relate seus recursos, alguns dispositivos retornam valores incorretos para esse método. Antes de copiar um arquivo para um dispositivo, talvez você queira perguntar ao usuário se a reprodução é pretendida e, nesse caso, tentar transcodificar o arquivo para um dos formatos relatados do dispositivo (ou um formato razoável, se o dispositivo solicitar suporte para qualquer formato). Outra abordagem é assumir que todos os formatos listados especificamente como com suporte pelo dispositivo são destinados à reprodução, e todos os outros arquivos devem ser transferidos sem modificações.

Depois de descobrir o formato do arquivo a ser transferido e os formatos com suporte de um dispositivo, você pode decidir qual é o melhor formato de destino para transcodificação.

No passado, era comum que um aplicativo retornasse zero para uma propriedade para indicar o suporte para qualquer valor dessa propriedade. Por exemplo, um valor de zero para [**\_ WAVEFORMATEX**](-waveformatex.md). nSamplesPerSec indicaria suporte para qualquer taxa de bits. Agora, a maneira recomendada para indicar o suporte para qualquer valor é especificar os \_ valores válidos de prop Enumeração SqlEnum \_ \_ \_ \_ any em [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md). ValidValuesForm. Algumas propriedades, porém, podem retornar legitimamente zero para indicar suporte específico. Por exemplo, se [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage for definido como zero, isso indicará um \_ bitmap RGB de BI. As exceções para valores zero são indicadas na documentação para as estruturas relevantes.

No entanto, é importante observar que os dispositivos geralmente não relatam seus recursos de formato corretamente ou de forma padrão. Por exemplo, os dispositivos geralmente relatam que oferecem suporte a qualquer formato, quando, na verdade, eles só podem manipular formatos específicos ou taxas de bits específicas em um tipo de formato. Cabe a você decidir se seu aplicativo deve aceitar esses relatórios ou se deve assumir algum tipo de limite superior para as capacidades de reprodução de um dispositivo (por exemplo, 192 kbps).

O método recomendado para solicitar o suporte ao formato de um dispositivo é [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Se esse método não tiver suporte, seu aplicativo deverá fazer fallback em [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport**, ao contrário de **GetFormatSupport2**, não retorna informações de vídeo.

Como um aplicativo solicita os recursos de formato de um dispositivo depende de qual interface o aplicativo dá suporte. Para obter mais detalhes, consulte os seguintes tópicos:

-   [Obtendo recursos de formato em dispositivos que dão suporte a IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Obtendo recursos de formato em dispositivos que dão suporte apenas a IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




