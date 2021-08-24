---
title: Lendo áudio multicanal
description: Lendo áudio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows SDK de Formato de Mídia, leitura de áudio multicanal
- ASF (Advanced Systems Format), leitura de áudio multicanal
- ASF (Formato de Sistemas Avançados), leitura de áudio multicanal
- ASF (Advanced Systems Format), áudio multicanal
- ASF (Formato de Sistemas Avançados), áudio multicanal
- codecs, leitura de áudio multicanal
- áudio multicanal, leitura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ba314c6f2579bb18cd73593a775089c4b04b1c4a8ecd34868af911da29a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658526"
---
# <a name="reading-multichannel-audio"></a>Lendo áudio multicanal

O codec Windows Media Audio 9 Professional pode codificar áudio multicanal (mais de dois canais). Ao ler um arquivo com áudio multicanal, você deve configurar a saída corretamente ou o áudio será entregue em uma qualidade inferior e em estéreo. Para definir uma saída para entrega de áudio multicanal, você deve definir duas configurações de saída: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.

Definir g \_ wszEnableDiscreteOutput como **TRUE** define o codec para fornecer saída de áudio de alta definição. O áudio de alta definição é codificado pelo codec Windows Media Audio 9 com exemplos de 24 bits em estéreo ou em vários canais. Se essa configuração for **FALSE,** somente a saída estéreo de 16 bits será entregue.

O número de alto-falantes no computador em reprodução é definido com g \_ wszSpeakerConfig. Essa configuração é um **valor DWORD** definido como uma das constantes do alto-falante DirectSound listadas na tabela a seguir. Para resolver esses nomes constantes para o compilador, você deve incluir dsound.h.



| Constante             | Valor      | Descrição                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | O áudio é passado diretamente, sem ser configurado para alto-falantes. |
| DSSPEAKER \_ HEADSET | 0x00000001 | O computador cliente está equipado com fones de ouvido.                             |
| DSSPEAKER \_ MONO      | 0x00000002 | O computador cliente está equipado com um alto-falante deural.                     |
| DSSPEAKER \_ QUAD      | 0x00000003 | O computador cliente é equipado com alto-falantes quadrônicos.                  |
| DSSPEAKER \_ ESTÉREO    | 0x00000004 | O computador cliente é equipado com alto-falantes estéreos.                        |
| DSSPEAKER \_ SURROUND  | 0x00000005 | O computador cliente é equipado com alto-falantes de som surround de quatro canais.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | O computador cliente é equipado com cinco alto-falantes e um subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | O computador cliente é equipado com sete alto-falantes e um subwoofer.         |



 

Para definir essas configurações, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Por fim, para que os canais sejam produzidos discretamente, sem dobra para estéreo, você deve definir o tipo de mídia correto na saída seguindo estas etapas:

1.  Chame [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos com suporte para a saída de áudio relevante. Os índices de formato de saída são baseados em zero.
2.  Para cada formato com suporte, chame [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) para recuperar a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) no objeto de propriedades de mídia de saída.
3.  Chame [**IWMMediaProps::GetMediaType para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) recuperar o tipo de mídia.
4.  Se o tipo de mídia recuperado for o tipo multicanal desejado, de definido chamando [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Depois de definir a saída discreta e a configuração do locutor, os formatos de saída enumerados pelo leitor devem incluir formatos multicanal que usam a estrutura [**WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) Se você enumerar os formatos de saída antes de definir as propriedades, somente os formatos com 1 ou 2 canais e um máximo de 16 bits por canal serão incluídos. Assim como com outros formatos de áudio, você deve usar apenas os formatos enumerados pelo leitor; não configure seu próprio.

> [!Note]  
> Você só poderá fazer a saída de áudio multicanal se seu aplicativo estiver em execução no Microsoft Windows XP ou em uma versão posterior do Microsoft Windows.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Saída Configurações**](output-settings.md)
</dt> <dt>

[**Trabalhando com High-Resolution áudio PCM**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 