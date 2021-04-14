---
description: Enumerando tipos de áudio para modos de codificação específicos
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerando tipos de áudio para modos de codificação específicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370525"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Enumerando tipos de áudio para modos de codificação específicos (Microsoft Media Foundation)

Os tipos de mídia de entrada e saída aceitos pelo codificador de áudio são muito estruturados. Você deve obter os tipos de saída com suporte chamando o método **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**. Depois de obter um tipo de saída, você não deve alterá-lo.

Se você quiser usar um modo de codificação diferente de uma passagem CBR, deverá definir o modo e, em seguida, enumerar os tipos de saída para esse modo; o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos. As propriedades que controlam o modo de codificação são [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Quando o modo é definido no codificador, você deve enumerar e selecionar um tipo de saída, usando-o sem alteração, assim como acontece com a CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identificando tipos de VBR com base na qualidade

O procedimento para identificar tipos de VBR com base na qualidade depende se o codificador está agindo como um DMO (objeto de mídia do DirectX) ou atuando como uma MFT (Media Foundation transformação). Para obter informações sobre quando um codificador atua como um DMO ou uma MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).

Quando um codificador de áudio está agindo como DMO e você configura o codificador para usar a VBR de uma passagem, ele enumera todos os tipos de saída com suporte. No entanto, normalmente você desejará selecionar um tipo de VBR de passagem com base no parâmetro de qualidade. O codificador coloca o valor de qualidade para os tipos de saída de VBR de uma passagem no membro **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** apontada pelo **tipo de \_ mídia DMO \_ . pbFormat**.

Esse valor é armazenado no seguinte formato: 0x7FFFFFXX, em que XX é o valor de qualidade (de 0 a 100). Por exemplo, o valor de **nAvgBytesPerSec** de 0x7FFFFF62 especifica o nível de qualidade 98 (0x62 = 98).

O exemplo a seguir mostra como verificar o nível de qualidade de um formato quando o codificador está agindo como um DMO.


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



Quando o codificador está agindo como um MFT e enumera um tipo de saída em uma chamada para **GetAvailableOutputType**, você pode consultar o MFT para a **propriedade \_ \_ \_ \_ VBRQUALITY enumerada mais recentemente do MFPKEY** . O valor retornado indica a qualidade de VBR do tipo de mídia de saída retornado mais recentemente. Em seguida, você pode usar esse valor para definir a propriedade [**MFPKEY \_ desejada \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) do codificador.

## <a name="setting-peak-constraints"></a>Definindo restrições de pico

Para uma taxa de bits variável baseada em qualidade (uma passagem) e uma VBR de duas passagens não restringida, nenhuma configuração adicional é necessária após a recuperação do tipo de saída. Para usar a taxa de bits de pico restrito, recupere um tipo de saída com VBR habilitado e duas passagens definidas. Esse tipo, sem alteração, descreve as configurações de VBR não restringidas. Para definir as restrições de pico, defina as propriedades [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) e [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando codificação de áudio](configuringaudioencoding.md)
</dt> <dt>

[Localizando tipos de saída do codificador de áudio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Usando a codificação Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Usando a codificação de VBR](usingvbrencoding.md)
</dt> </dl>

 

 



