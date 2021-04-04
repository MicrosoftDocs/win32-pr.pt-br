---
title: Para desentrelaçar vídeo
description: Para desentrelaçar vídeo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- SDK do Windows Media Format, vídeo desentrelaçado
- SDK do Windows Media Format, telecineon inverso
- SDK do Windows Media Format, telecineon
- ASF (Advanced Systems Format), vídeo desentrelaçado
- ASF (formato de sistemas avançados), vídeo desentrelaçado
- Formato de sistema avançado (ASF), inverso
- ASF (formato de sistemas avançados), telecineon inverso
- Formato de sistema avançado (ASF), telecineon
- ASF (formato de sistemas avançados), telecineon
- vídeo desentrelaçado
- inverso, sobre
- telecineon, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007126"
---
# <a name="to-deinterlace-video"></a>Para desentrelaçar vídeo

Algumas fontes de vídeo, como cartões de captura de vídeo, fornecem dados de vídeo para exibição entrelaçada. Cada quadro de vídeo entrelaçado é composto de dois campos. O campo superior contém a primeira linha de vídeo e todas as outras linhas posteriormente. O campo inferior contém a segunda linha de vídeo e todas as outras linhas posteriormente. Portanto, um campo contém todas as linhas numeradas pares e a outra contém todas as linhas ímpares. Os campos que compõem um quadro representam tempos de apresentação um pouco diferentes para que, quando intercalados, não formam uma imagem estática.

Quando você deseja exibir vídeo em um monitor de computador, cada quadro do vídeo deve ser exibido como uma imagem (esse método de exibir o vídeo de um quadro inteiro por vez é chamado de vídeo *progressivo* ). Se você exibir vídeo entrelaçado progressivamente, os quadros podem não parecer corretos, devido à diferença de tempo entre os dois campos. O codec de vídeo do Windows Media e o codec de perfil avançado do vídeo do Windows Media oferecem suporte a um recurso de pré-processamento que converte conteúdo entrelaçado em quadros progressivos.

Para que o codec desentrelaçar o vídeo de entrada, chame o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) . A configuração a ser usada é g \_ wszDeinterlaceMode. Defina o modo de desentrelaçamento como um dos valores a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>A entrada é progressiva. Use essa configuração para parar de desentrelaçar quando você tiver definido anteriormente o modo de desentrelaçamento para outro valor.</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>Selecione este modo para misturar os campos pares e ímpares de um quadro entrelaçado (usando um mecanismo de compensação de movimento). Benefícios<br/>
<ul>
<li>Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</li>
<li>O codec de vídeo do Windows Media produz vídeo compactado de alta qualidade.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>Selecione esse modo quando a resolução de saída for metade ou menor da resolução de entrada. Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels e a resolução de vídeo de saída for de 320 x 240 pixels. Benefícios<br/>
<ul>
<li>Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>Selecione esse modo quando a resolução de saída for metade, ou menos, da resolução de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta. Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo de saída for 320 x 240 pixels em 60 quadros/s. Benefícios<br/>
<ul>
<li>Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</li>
<li>O movimento completo dos campos entrelaçados é capturado.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>Selecione este modo para converter o vídeo telecineon de 30 quadros/s nos 24 quadros/s do filme original. Benefícios<br/>
<ul>
<li>A qualidade da compactação melhora significativamente porque apenas 24 quadros/s em vez de 30 quadros/s precisam ser codificados.</li>
<li>Como o resultado é progressivo, a mesma compactação e os benefícios de exibição de desentrelaçamento são percebidos.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>Selecione esse modo quando a resolução vertical de saída for metade, ou menos, da resolução vertical de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta. Por exemplo, a resolução de vídeo vertical de entrada é 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo vertical de saída é 320 x 240 pixels em 60 quadros/s. Benefícios<br/>
<ul>
<li>Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</li>
<li>O movimento completo dos campos entrelaçados é capturado.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Para conteúdo misto, defina o modo de desentrelaçamento conforme necessário antes de passar amostras de um novo tipo. Por exemplo, para iniciar a codificação com a entrada progressiva, você não precisa definir nenhum modo de desentrelaçamento. Se alguns exemplos exigirem desentrelaçamento normal, você deverá definir o modo de desentrelaçamento para o WM \_ DM \_ desentrelaçar \_ normal. Para processar amostras progressivas adicionais, você deve definir o modo de desentrelaçamento para o WM \_ DM não \_ entrelaçado.

## <a name="inverse-telecine-settings"></a>Configurações de inversos

Para obter uma descrição do telecineon inverso, consulte [para usar o telecineon inverso](to-use-inverse-telecine.md).

Se você definir o modo de desentrelaçamento para o WM \_ DM \_ desentrelaçar \_ INVERSETELECINE, poderá especificar o padrão de telecineon do primeiro quadro de entrada chamando o [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). A configuração a ser usada é g \_ wszInitialPatternForInverseTelecine. Defina o padrão inicial como um dos valores a seguir.



| Valor                                              | Descrição                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| o WM \_ DM \_ desabilita o \_ \_ \_ modo coerente                | Especifica que a mídia de entrada passou pelo processo de telecineon, mas que os quadros não estão mais em um padrão previsível. Isso geralmente indica que a mídia foi editada após o processamento de telecineon. Quando você usa essa configuração, o codec tenta reconstruir os quadros originais por conta própria. |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ em \_ clip \_ é \_ AA \_ Top    | Especifica que o campo superior do quadro AA é o primeiro exemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BB na \_ parte superior    | Especifica que o campo superior do quadro BB é o primeiro exemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BC \_ superior    | Especifica que o campo superior do quadro BC é o primeiro exemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ CD \_ superior    | Especifica que o campo superior do quadro do CD é o primeiro exemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ DD \_ Top    | Especifica que o campo superior do quadro DD é o primeiro exemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ em \_ clip \_ é \_ AA \_ Bottom | Especifica que o campo inferior do quadro AA é o primeiro exemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BB \_ inferior | Especifica que o campo inferior do quadro BB é o primeiro exemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BC- \_ Bottom | Especifica que o campo inferior do quadro BC é o primeiro exemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ o \_ primeiro \_ quadro \_ no \_ clipe \_ é o \_ CD \_ inferior | Especifica que o campo inferior do quadro do CD é o primeiro exemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ DD \_ Bottom | Especifica que o campo inferior do quadro DD é o primeiro exemplo.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> </dl>

 

 





