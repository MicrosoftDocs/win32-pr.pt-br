---
title: Captura de fluxo de um dispositivo MCI
description: Captura de fluxo de um dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (interface de controle de mídia), captura de streaming
- WM_CAP_SET_MCI_DEVICE mensagem
- macro capSetMCIDeviceName
- WM_CAP_GET_MCI_DEVICE mensagem
- macro capGetMCIDeviceName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498773"
---
# <a name="streaming-capture-from-an-mci-device"></a>Captura de fluxo de um dispositivo MCI

Os dispositivos MCI aumentam a operação de captura em captura em tempo real e captura de quadro de etapa. Você pode especificar o dispositivo MCI, como um VIDEODISC ou um gravador de fita de vídeo (VCR), agindo como a fonte de vídeo para a operação de captura usando a mensagem do [**\_ \_ \_ \_ dispositivo MCI de conjunto de Cap do WM**](wm-cap-set-mci-device.md) (ou a macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ) e especificando o nome do dispositivo. Você também pode recuperar o nome do dispositivo definido atualmente usando a mensagem de [**\_ \_ \_ \_ dispositivo MCI do WM Cap Get**](wm-cap-get-mci-device.md) (ou a macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) ).

Na captura em tempo real, a janela de captura sincroniza a operação de captura e compensa os atrasos associados ao posicionamento da fonte de vídeo MCI e a inicialização dos recursos (como buffers de captura) necessários para a captura de dados. A janela de captura espera que um dispositivo de vídeo MCI válido seja instalado no sistema para capturar dados dessa maneira.

As especificações para controlar um dispositivo MCI são armazenadas nos membros da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . As fontes de vídeo compatíveis com MCI incluem VCRs e laserdiscs. Se o membro **fMCIControl** dessa estrutura for definido como **true**, a janela de captura coordenará a operação MCI. A janela de captura usa os parâmetros especificados nos membros **dwMCIStartTime** e **dwMCIStopTime** para obter as posições de início e de parada, em milissegundos, da sequência. Se o valor de **fMCIControl** for **false**, a fonte de vídeo não será tratada como um dispositivo MCI e o conteúdo de **dwMCIStartTime** e **dwMCIStopTime** serão ignorados.

Você pode usar o player de mídia para verificar rapidamente se um dispositivo de vídeo MCI está conectado corretamente ao sistema. A reprodução de um dispositivo com o player de mídia verifica se a configuração do MCI do dispositivo está correta. Se uma imagem aparecer na tela de vídeo, a fonte de vídeo será conectada corretamente ao hardware de captura.

Na captura de quadros de etapa, a janela de captura sincroniza a operação de captura e compensa os atrasos associados ao posicionamento da fonte de vídeo MCI e a inicialização dos recursos necessários para a captura de dados. Além disso, a janela de captura garante que nenhum quadro seja Descartado; Ele percorre os quadros de vídeo individualmente, garantindo que o quadro seja capturado e armazenado antes de capturar o próximo quadro no fluxo de vídeo.

As especificações para controlar a captura de quadro de etapa são armazenadas nos membros da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . A captura de quadro de etapa usa os seguintes membros, além dos membros usados para captura em tempo real: **fStepMCIDevice**, **fStepCaptureAt2x** e **wStepCaptureAverageFrames**. Se o membro **fStepMCIDevice** for definido como **true**, a janela de captura coordenará a captura de quadro de etapa. A janela de captura usa os parâmetros especificados nos membros **dwMCIStartTime** e **dwMCIStopTime** para as posições de início e parada, em milissegundos, da sequência. A janela de captura usa **fStepCaptureAt2x** para determinar se o hardware de captura deve capturar quadros de vídeo em duas vezes a resolução normal e usa **wStepCaptureAverageFrames** para especificar o número de vezes que cada quadro na operação de captura é amostrado.

Se **fStepMCIDevice** for **false**, a captura em tempo real será usada em vez de captura de quadro de etapa e o conteúdo de **fStepCaptureAt2x** e **wStepCaptureAverageFrames** serão ignorados.

Se uma captura de quadro de etapa for especificada e **fStepCaptureAt2x** for definido como **true**, o hardware de captura será capturado em duas vezes a resolução especificada. (As resoluções de altura e largura são duplas.) O software interpola os pixels na imagem de resolução mais alta para produzir a imagem na resolução especificada. Essa forma de média pode melhorar a definição de borda de imagens em um quadro. Você pode habilitar essa opção se o hardware não oferecer suporte a Decimation baseadas em hardware e você estiver capturando no formato RGB.

> [!Note]  
> Se o hardware der suporte a Decimation com base em hardware, ele poderá capturar amostras em uma taxa mais alta do que a especificada e usar esses exemplos adicionais para obter definições de cores mais consistentes com a imagem original. Os exemplos adicionais são descartados após serem usados e o hardware passa amostras para o driver de captura na taxa especificada.

 

Se uma captura de quadro de etapa for especificada, o membro **wStepCaptureAverageFrames** especificará o número de vezes que um quadro é amostrado ao criar um quadro com base no exemplo médio. Essa técnica de média reduz o ruído de digitalização aleatória que aparece em um quadro. Um valor típico para o número de médias é 5.

Para obter mais informações sobre o MCI, consulte [MCI](mci.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturar variações](capture-variations.md)
</dt> </dl>

 

 




