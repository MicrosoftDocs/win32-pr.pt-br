---
title: Para desentrelaçar vídeo
description: Para desentrelaçar vídeo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows SDK do formato de mídia, vídeo desentrelaçado
- Windows SDK do formato de mídia, telecineon inverso
- Windows SDK do formato de mídia, telecineon
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
ms.openlocfilehash: 1ef1d1a6fcee3bf43d2fb4451d4ef129e595471e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475762"
---
# <a name="to-deinterlace-video"></a>Para desentrelaçar vídeo

Algumas fontes de vídeo, como cartões de captura de vídeo, fornecem dados de vídeo para exibição entrelaçada. Cada quadro de vídeo entrelaçado é composto de dois campos. O campo superior contém a primeira linha de vídeo e todas as outras linhas posteriormente. O campo inferior contém a segunda linha de vídeo e todas as outras linhas posteriormente. Portanto, um campo contém todas as linhas numeradas pares e a outra contém todas as linhas ímpares. Os campos que compõem um quadro representam tempos de apresentação um pouco diferentes para que, quando intercalados, não formam uma imagem estática.

Quando você deseja exibir vídeo em um monitor de computador, cada quadro do vídeo deve ser exibido como uma imagem (esse método de exibir o vídeo de um quadro inteiro por vez é chamado de vídeo *progressivo* ). Se você exibir vídeo entrelaçado progressivamente, os quadros podem não parecer corretos, devido à diferença de tempo entre os dois campos. o codec de vídeo de mídia Windows e o codec de perfil avançado de vídeo de mídia Windows oferecem suporte a um recurso de pré-processamento que converte conteúdo entrelaçado em quadros progressivos.

Para que o codec desentrelaçar o vídeo de entrada, chame o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) . A configuração a ser usada é g \_ wszDeinterlaceMode. Defina o modo de desentrelaçamento como um dos valores a seguir.




| Valor | Descrição | 
|-------|-------------|
| WM_DM_NOTINTERLACED | A entrada é progressiva. Use essa configuração para parar de desentrelaçar quando você tiver definido anteriormente o modo de desentrelaçamento para outro valor. | 
| WM_DM_DEINTERLACE_NORMAL | Selecione este modo para misturar os campos pares e ímpares de um quadro entrelaçado (usando um mecanismo de compensação de movimento). Benefícios<br /><ul><li>Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</li><li>o codec de vídeo de mídia Windows produz vídeo compactado de alta qualidade.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZE | Selecione esse modo quando a resolução de saída for metade ou menor da resolução de entrada. Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels e a resolução de vídeo de saída for de 320 x 240 pixels. Benefícios<br /><ul><li>Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE | Selecione esse modo quando a resolução de saída for metade, ou menos, da resolução de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta. Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo de saída for 320 x 240 pixels em 60 quadros/s. Benefícios<br /><ul><li>Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</li><li>O movimento completo dos campos entrelaçados é capturado.</li></ul> | 
| WM_DM_DEINTERLACE_INVERSETELECINE | Selecione este modo para converter o vídeo telecineon de 30 quadros/s nos 24 quadros/s do filme original. Benefícios<br /><ul><li>A qualidade da compactação melhora significativamente porque apenas 24 quadros/s em vez de 30 quadros/s precisam ser codificados.</li><li>Como o resultado é progressivo, a mesma compactação e os benefícios de exibição de desentrelaçamento são percebidos.</li></ul> | 
| WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE | Selecione esse modo quando a resolução vertical de saída for metade, ou menos, da resolução vertical de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta. Por exemplo, a resolução de vídeo vertical de entrada é 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo vertical de saída é 320 x 240 pixels em 60 quadros/s. Benefícios<br /><ul><li>Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</li><li>O movimento completo dos campos entrelaçados é capturado.</li></ul> | 




 

Para conteúdo misto, defina o modo de desentrelaçamento conforme necessário antes de passar amostras de um novo tipo. Por exemplo, para iniciar a codificação com a entrada progressiva, você não precisa definir nenhum modo de desentrelaçamento. Se alguns exemplos exigirem desentrelaçamento normal, você deverá definir o modo de desentrelaçamento para o WM \_ DM \_ desentrelaçar \_ normal. Para processar amostras progressivas adicionais, você deve definir o modo de desentrelaçamento para o WM \_ DM não \_ entrelaçado.

## <a name="inverse-telecine-settings"></a>Configurações de inverso

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

 

 





