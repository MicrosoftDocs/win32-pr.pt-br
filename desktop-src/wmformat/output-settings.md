---
title: Configurações de saída
description: Configurações de saída
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- SDK do Windows Media Format, constantes globais
- ASF (Advanced Systems Format), constantes globais
- ASF (formato de sistemas avançados), constantes globais
- constantes globais, lista de
- SDK do Windows Media Format, constantes
- ASF (Advanced Systems Format), constantes
- ASF (formato de sistemas avançados), constantes
- constantes, lista de
- SDK do Windows Media Format, configurações de saída
- ASF (Advanced Systems Format), configurações de saída
- ASF (formato de sistemas avançados), configurações de saída
- configurações de saída
- leitores síncronos, configurações de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084340"
---
# <a name="output-settings"></a>Configurações de saída

As constantes globais a seguir são usadas para identificar as configurações de saída para o leitor e o objeto leitor síncrono.



| Constante global                | \_tipo de \_ dados attr WMT  | Descrição de *uma* era                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **WMT \_ tipo \_ bool**  | Se for true, o leitor fornecerá quadros entrelaçados, se houver suporte na saída.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **WMT \_ tipo \_ bool**  | Se for true, essa saída terá um thread dedicado criado para entrega de seus exemplos. Sem suporte no leitor síncrono.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **WMT \_ tipo \_ bool**  | Se for true, os exemplos para essa saída serão entregues assim que estiverem disponíveis no leitor. Isso pode resultar em amostras dessa saída sendo entregue fora de ordem e antes das amostras correspondentes de outras saídas.                                                                                            |
| g \_ wszDynamicRangeControl      | **WMT \_ tipo \_ DWORD** | Especifica o nível do controle de intervalo dinâmico a ser usado para a saída. Defina como um valor de 0 a 2, em que 0 indica que nenhum controle de intervalo dinâmico (o padrão) e 2 é o nível máximo do controle de intervalo dinâmico (o menor intervalo dinâmico).                                                                                |
| g \_ wszEarlyDataDelivery        | **WMT \_ tipo \_ DWORD** | Tempo, em milissegundos, que especifica o quanto antes para entregar os exemplos. Se for maior que zero, os exemplos dessa saída serão recuperados e decodificados para que os exemplos sejam entregues antes dos exemplos de outras saídas. Normalmente, o leitor fornece exemplos em ordem de tempo de apresentação.         |
| g \_ wszEnableDiscreteOutput     | **WMT \_ tipo \_ bool**  | Se for true, o leitor habilitará a saída de áudio de alta definição e multicanal. Essa configuração só é válida para fluxos de áudio codificados com o codec Windows Media Audio 9 Professional. Se essa configuração for definida como true, você também deverá especificar a configuração do alto-falante do computador cliente, definindo g \_ wszSpeakerConfig. |
| g \_ wszEnableFrameInterpolation | **WMT \_ tipo \_ bool**  | Se for true, o codec entregará o fluxo de vídeo em uma [*taxa de quadros*](wmformat-glossary.md)superior, interpolando os quadros forma algorítmica.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **WMT \_ tipo \_ bool**  | Se for true, os dados deverão ser decodificados o mais tarde possível. Sem suporte no leitor síncrono.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **WMT \_ tipo \_ bool**  | Se for true, o exemplo exigirá que a amostra anterior seja descompactada. Essa configuração se aplica somente a quadros Delta em vídeo compactado e é somente leitura.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **WMT \_ tipo \_ bool**  | Se for true, essa saída usará o esquema de ocultação de erro de áudio embaralhado. Essa é uma configuração válida somente para saídas de áudio.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **WMT \_ tipo \_ bool**  | Se for true, um único buffer de saída deverá ser usado (por exemplo, um® de buffer de vídeo do DirectDraw). Sem suporte no leitor síncrono.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **WMT \_ tipo \_ bool**  | Se for false, o vídeo não será dimensionado. (Não deve haver nenhuma alteração na resolução.)                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **WMT \_ tipo \_ DWORD** | Se a decodificação de áudio multicanal estiver habilitada definindo g \_ wszEnableDiscreteOutput, essa configuração especificará a configuração do alto-falante do computador cliente. Defina como uma das constantes de configuração do alto-falante DirectSound.                                                                                                   |
| g \_ wszStreamLanguage           | **WMT \_ tipo de \_ palavra**  | O índice na lista de idiomas do idioma a ser entregue para essa saída. Usado para saídas que representam fluxos mutuamente exclusivos por linguagem.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **WMT \_ tipo \_ bool**  | Se for true, o leitor fornecerá durações de amostra precisas.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **WMT \_ tipo \_ bool**  | Se for true, o leitor incluirá o formato de interface digital Sony/Phillips (S/PDIF) nos tipos de saída enumerados.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




