---
title: Para usar o controle de intervalo dinâmico
description: Para usar o controle de intervalo dinâmico
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- SDK do Windows Media Format, controle de intervalo dinâmico
- SDK do Windows Media Format, codec do Windows Media Audio 9 Professional
- SDK do Windows Media Format, codec de áudio do Windows Media 9 sem perdas
- ASF (Advanced Systems Format), codec do Windows Media Audio 9 Professional
- ASF (formato de sistemas avançados), codec do Windows Media Audio 9 Professional
- ASF (Advanced Systems Format), codec de áudio do Windows Media 9 Lossless
- ASF (formato de sistemas avançados), codec de áudio do Windows Media 9 Lossless
- ASF (Advanced Systems Format), controle de intervalo dinâmico
- ASF (formato de sistemas avançados), controle de intervalo dinâmico
- controle de intervalo dinâmico
- codecs, codec de áudio do Windows Media 9 sem perdas
- codecs, codec do Windows Media Audio 9 Professional
- Codec sem perdas do Windows Media Audio 9, controle de intervalo dinâmico
- Codec do Windows Media Audio 9 Professional, controle de intervalo dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105810737"
---
# <a name="to-use-dynamic-range-control"></a>Para usar o controle de intervalo dinâmico

O intervalo dinâmico de uma parte do conteúdo de áudio é basicamente a diferença entre o volume mais baixo e o volume máximo. Se o intervalo dinâmico do conteúdo for muito alto, os usuários poderão se encontrar ajustando o volume repetidamente durante a reprodução. Por exemplo, os filmes com frequência têm um intervalo dinâmico alto. Geralmente, quando o volume é ajustado para que a caixa de diálogo possa ser compreendida durante os bastidores silenciosos, outras partes do filme com efeitos musicais ou sonoros são mais altos do que o desejado.

Os codecs do Windows Media Audio 9 Professional e Windows Media Audio 9 Lossless dão suporte a um recurso chamado controle de intervalo dinâmico. No momento da codificação, o codec calcula os valores de amplitude de pico e média no conteúdo, e o objeto gravador armazena esses valores nos metadados para o fluxo quando a codificação é concluída. Opcionalmente, um aplicativo também pode gravar valores de "destino" como metadados que os aplicativos do Player e o decodificador podem usar como dicas ao reproduzir o arquivo. No tempo de reprodução, um aplicativo pode especificar o nível de controle de intervalo dinâmico a ser aplicado ao fluxo de áudio.

O Windows Media Player implementa o controle de intervalo dinâmico como o recurso de modo silencioso.

## <a name="when-to-use-dynamic-range-control"></a>Quando usar o controle de intervalo dinâmico

O controle de intervalo dinâmico pode alterar o som do conteúdo. Por esse motivo, você não deve configurar seu aplicativo para usar o controle de intervalo dinâmico automaticamente. Em vez disso, forneça aos usuários a capacidade de ativar ou desativar o controle de intervalo dinâmico, conforme necessário.

## <a name="using-dynamic-range-control"></a>Usando o controle de intervalo dinâmico

No tempo de reprodução, o controle de intervalo dinâmico é ativado usando a configuração de saída g \_ wszDynamicRangeControl. Use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para definir a configuração. Um valor de zero (o padrão) indica que o intervalo dinâmico não deve ser alterado. Um valor de 1 ou 2 sinaliza o codec para executar o controle de intervalo dinâmico, em que 1 é um nível moderado de compactação de intervalo dinâmico e 2 é um alto nível de compactação de intervalo dinâmico.

No momento da codificação ou no tempo de reprodução, você pode dar ao codec o destino valores de PCM para os níveis de pico e médio definindo os atributos [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) e [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) , respectivamente. Esses valores são armazenados como atributos de metadados e devem ser acessados usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) . Quando você codifica um fluxo de áudio usando o codec Professional ou Lossless, os atributos [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) e [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) são definidos automaticamente para os níveis de pico e médio do conteúdo original. Os valores de destino são definidos como os mesmos valores das referências por padrão.

O decodificador no tempo de reprodução calcula o intervalo dinâmico com base no nível selecionado do controle de intervalo dinâmico e os valores de destino (se houver algum especificado). Os intervalos possíveis são mostrados na tabela a seguir.



| Settings                                                                | Intervalo de áudio entregue                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (quaisquer valores de destino)                       | Mesmo intervalo do conteúdo original.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (valores de destino iguais aos valores de referência) | O nível médio é mantido e os picos são confinados para a média de + 12 dB.                                                    |
| g \_ wszDynamicRangeControl = 2 (valores de destino iguais aos valores de referência) | O nível médio é mantido e os picos são confinados no banco de e médio + 6 dB.                                                     |
| g \_ wszDynamicRangeControl = 1 (valores de destino especificados)                 | Nível médio definido como o valor médio de destino e o pico confinados para o valor de pico de destino.                                   |
| g \_ wszDynamicRangeControl = 2 (valores de destino especificados)                 | Nível médio definido como o valor médio de destino e picos refinados à mediana dos valores de pico de destino e média de destino. |



 

Observe que o controle de intervalo dinâmico é um recurso de decodificação apenas e existe somente como metadados no próprio arquivo. Essas configurações não têm efeito sobre o conteúdo armazenado no arquivo, a menos que você instrua especificamente o decodificador para usá-los. O Windows Media Format SDK não fornece métodos para modificar o intervalo dinâmico dos dados de áudio no momento da codificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> </dl>

 

 




