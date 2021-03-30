---
title: Lendo áudio de multicanal
description: Lendo áudio de multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lendo áudio multicanal
- ASF (Advanced Systems Format), lendo áudio de multicanal
- ASF (formato de sistemas avançados), lendo áudio de multicanal
- ASF (Advanced Systems Format), áudio multicanal
- ASF (formato de sistemas avançados), áudio de multicanal
- codecs, lendo áudio de multicanal
- áudio de multicanal, lendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641638"
---
# <a name="reading-multichannel-audio"></a>Lendo áudio de multicanal

O codec Windows Media Audio 9 Professional pode codificar áudio multicanal (mais de dois canais). Ao ler um arquivo com áudio multicanal, você deve configurar a saída corretamente ou o áudio será entregue em uma qualidade menor e em estéreo. Para definir uma saída para entrega de áudio multicanal, você deve definir duas configurações de saída: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.

A definição \_ de g wszEnableDiscreteOutput como **true** define o codec para fornecer saída de áudio de alta definição. Áudio de alta definição é codificado pelo codec do Windows Media Audio 9 com amostras de 24 bits em estéreo ou vários canais. Se essa configuração for **falsa**, somente a saída estéreo de 16 bits será entregue.

O número de alto-falantes no computador de jogo é definido com g \_ wszSpeakerConfig. Essa configuração é um valor **DWORD** definido como uma das constantes de alto-falante DirectSound listadas na tabela a seguir. Para resolver esses nomes de constantes para seu compilador, você deve incluir dsound. h.



| Constante             | Valor      | Descrição                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ directout | 0x00000000 | O áudio é transmitido diretamente, sem ser configurado para os alto-falantes. |
| \_fone de ouvido DSSPEAKER | 0x00000001 | O computador cliente está equipado com fones de ouvido.                             |
| DSSPEAKER \_ mono      | 0x00000002 | O computador cliente está equipado com um monaural palestrante.                     |
| DSSPEAKER \_ Quad      | 0x00000003 | O computador cliente está equipado com alto-falantes Quadraphonic.                  |
| estéreo de DSSPEAKER \_    | 0x00000004 | O computador cliente está equipado com alto-falantes estéreo.                        |
| \_surround DSSPEAKER  | 0x00000005 | O computador cliente está equipado com alto-falantes surround-sound.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | O computador cliente é equipado com cinco alto-falantes e um subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | O computador cliente está equipado com sete palestrantes e um subwoofer.         |



 

Para definir essas configurações, use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Por fim, para que os canais sejam impressos de forma discreta, sem dobra para estéreo, você deve definir o tipo de mídia correto na saída seguindo estas etapas:

1.  Chame [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos com suporte para a saída de áudio relevante. Os índices de formato de saída são baseados em zero.
2.  Para cada formato com suporte, chame [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) para recuperar a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) no objeto de propriedades de mídia de saída.
3.  Chame [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) para recuperar o tipo de mídia.
4.  Se o tipo de mídia recuperado for o tipo de multicanal desejado, defina-o chamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Depois de definir a saída discreta e a configuração do alto-falante, os formatos de saída enumerados pelo leitor devem incluir formatos multicanal que usam a estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) . Se você enumerar os formatos de saída antes de definir as propriedades, somente os formatos com 1 ou 2 canais e um máximo de 16 bits por canal serão incluídos. Assim como acontece com outros formatos de áudio, você deve usar apenas os formatos enumerados pelo leitor; Não configure seu próprio.

> [!Note]  
> Você poderá produzir áudio multicanal somente se seu aplicativo estiver em execução no Microsoft Windows XP ou em uma versão posterior do Microsoft Windows.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Configurações de saída**](output-settings.md)
</dt> <dt>

[**Trabalhando com High-Resolution áudio PCM**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 