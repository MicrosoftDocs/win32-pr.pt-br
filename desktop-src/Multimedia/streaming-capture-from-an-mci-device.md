---
title: Captura de streaming de um dispositivo MCI
description: Captura de streaming de um dispositivo MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Interface de Controle de Mídia), captura de streaming
- WM_CAP_SET_MCI_DEVICE mensagem
- Macro capSetMCIDeviceName
- WM_CAP_GET_MCI_DEVICE mensagem
- Macro capGetMCIDeviceName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d469465f47e908bda2512261ea638ad23e931a43cbb0449df676829469c3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892586"
---
# <a name="streaming-capture-from-an-mci-device"></a>Captura de streaming de um dispositivo MCI

Os dispositivos MCI ampliam a operação de captura em tempo real e captura de quadro-etapa. Você pode especificar o dispositivo MCI, como um videodisc ou um VCR (gravador de gravação de vídeo), atuando como a fonte de vídeo para sua operação de captura usando a mensagem [**WM \_ CAP SET \_ \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md) (ou a macro [**capSetMCIDeviceName)**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) e especificando o nome do dispositivo. Você também pode recuperar o nome do dispositivo atualmente definido usando a mensagem [**WM \_ CAP GET \_ \_ MCI \_ DEVICE**](wm-cap-get-mci-device.md) (ou a [**macro capGetMCIDeviceName).**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename)

Na captura em tempo real, a janela de captura sincroniza a operação de captura e compensa os atrasos associados ao posicionamento da fonte de vídeo MCI e à inicialização dos recursos (como buffers de captura) necessários para capturar dados. A janela de captura espera que um dispositivo de vídeo MCI válido seja instalado no sistema para capturar dados dessa maneira.

As especificações para controlar um dispositivo MCI são armazenadas nos membros da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) As fontes de vídeo compatíveis com MCI incluem VCRs e laserdiscs. Se o **membro fMCIControl** dessa estrutura estiver definido como **TRUE,** a janela de captura coordenará a operação MCI. A janela de captura usa os parâmetros especificados nos membros **dwMCIStartTime** e **dwMCIStopTime** para obter as posições inicial e de parada, em milissegundos, da sequência. Se o valor de **fMCIControl** for **FALSE,** a origem do vídeo não será tratada como um dispositivo MCI e o conteúdo de **dwMCIStartTime** e **dwMCIStopTime** será ignorado.

Você pode usar o Media Player para verificar rapidamente se um dispositivo de vídeo MCI está conectado corretamente ao sistema. A reprodução de um dispositivo com o Media Player verifica se a configuração de MCI do dispositivo está correta. Se uma imagem for exibida na exibição de vídeo, a fonte do vídeo será conectada corretamente ao hardware de captura.

Na captura de quadro-etapa, a janela de captura sincroniza a operação de captura e compensa os atrasos associados ao posicionamento da fonte de vídeo MCI e à inicialização dos recursos necessários para capturar dados. Além disso, a janela de captura garante que nenhum quadro seja descartado; ele passa pelos quadros de vídeo individualmente, garantindo que o quadro seja capturado e armazenado antes de capturar o próximo quadro no fluxo de vídeo.

As especificações para controlar a captura de quadro passo são armazenadas nos membros da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) A captura de quadro-passo usa os seguintes membros além dos membros usados para captura em tempo real: **fStepMCIDevice**, **fStepCaptureAt2x** e **wStepCaptureAverageFrames**. Se o **membro fStepMCIDevice** estiver definido como **TRUE,** a janela de captura coordenará a captura de quadro-etapa. A janela de captura usa os parâmetros especificados nos membros **dwMCIStartTime** e **dwMCIStopTime** para as posições inicial e parada, em milissegundos, da sequência. A janela de captura usa **fStepCaptureAt2x** para determinar se o hardware de captura deve capturar quadros de vídeo em duas vezes a resolução normal e usa **wStepCaptureAverageFrames** para especificar o número de vezes que cada quadro na operação de captura é amostrado.

Se **fStepMCIDevice** for **FALSE,** a captura em tempo real será usada em vez da captura de quadro passo e o conteúdo de **fStepCaptureAt2x** e **wStepCaptureAverageFrames serão ignorados.**

Se uma captura de quadro passo for especificada e **fStepCaptureAt2x** for definido como **TRUE,** o hardware de captura capturará duas vezes a resolução especificada. (As resoluções da altura e da largura são dobradas.) O software interpola os pixels na imagem de resolução mais alta para produzir a imagem na resolução especificada. Essa forma de média pode melhorar a definição de borda das imagens em um quadro. Você pode habilitar essa opção se o hardware não dá suporte à dizimação baseada em hardware e você está capturando no formato RGB.

> [!Note]  
> Se o hardware for compatível com a dizimação baseada em hardware, ele poderá capturar amostras a uma taxa mais alta do que o especificado e usar esses exemplos adicionais para obter definições de cores mais consistentes com a imagem original. Os exemplos adicionais são descartados depois que são usados e o hardware passa amostras para o driver de captura na taxa especificada.

 

Se uma captura de quadro passo for especificada, o membro **wStepCaptureAverageFrames** especificará o número de vezes que um quadro é amostrado ao criar um quadro com base na amostra média. Essa técnica de média reduz o ruído de digitalização aleatório que aparece em um quadro. Um valor típico para o número de médias é 5.

Para obter mais informações sobre a MCI, consulte [MCI](mci.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Variações de captura](capture-variations.md)
</dt> </dl>

 

 




