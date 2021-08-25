---
description: Informações de Parâmetro
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Informações de Parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe38cc9197df3ae22bcd72b824da5887647bca9e9d6101e3833d482fa907052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050766"
---
# <a name="parameter-information"></a>Informações de Parâmetro

O [**método IMediaParamInfo::GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) retorna uma estrutura [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) que descreve um parâmetro. Essa estrutura contém as seguintes informações:

-   O **membro mpType** indica o tipo de dados do valor do parâmetro. Para eficiência, todos os parâmetros são implementados como valores de ponto flutuante de 32 bits. A [**\_ enumeração MP TYPE**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) define se o valor deve ser interpretado como um inteiro, valor de ponto flutuante, booliana ou enumeração (série de inteiros).
-   O **membro de thecaps** indica a quais curvas esse parâmetro dá suporte. Se o tipo de dados for booliana ou enumeração, a única curva à qual o parâmetro pode dar suporte é "Jump".
-   Os **membros mpdMinValue** e **mpdMaxValue** definem os valores mínimo e máximo para esse parâmetro. Todas as curvas para esse parâmetro devem estar dentro desse intervalo.
-   O **membro mpdNeutralValue** é o valor padrão do parâmetro .
-   O **membro szLabel** é o nome do parâmetro e o membro **szUnitText** é o nome da unidade de medida para o parâmetro . Os exemplos podem incluir "Volume" e "Decibels", ou "Frequency" e "kHz". Ambas as cadeias de caracteres são em inglês e nunca são localizadas. O DMO pode fornecer versões localizadas por meio do [**método IMediaParamInfo::GetParamText.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext)

As informações de cada parâmetro permanecem fixas durante o tempo de vida do DMO. Portanto, o cliente pode consultar essas informações uma vez e, em seguida, em cache.

**Formatos de hora**

O cliente deve carimbo de data/hora dos dados de entrada, para que o DMO possa calcular os valores de parâmetro correspondentes. Por padrão, os carimbos de data/hora representam unidades de 100 nanossegundos, também chamado de tempo *de referência.* No entanto, essa unidade de tempo não é conveniente para todos os aplicativos, portanto, um DMO tem a opção de dar suporte a outros formatos de hora. Os formatos de hora são identificados pelo GUID.



| **GUID**              | Descrição                   |
|-----------------------|-------------------------------|
| REFERÊNCIA \_ DE TEMPO DE \_ GUID | Tempo de referência                |
| GUID \_ TIME \_ MUSIC     | PPQN (partes por trimestre) |
| EXEMPLOS \_ DE \_ TEMPO DE GUID   | Exemplos por segundo            |



 

Terceiros são incentivados a definir seus próprios formatos de tempo, conforme necessário. No entanto, todos os DMOs devem dar suporte ao tempo de referência. Isso fornece uma linha de base padrão que todos podem usar. Para determinar quantos formatos de tempo um DMO dá suporte, chame o método [**IMediaParamInfo::GetNumTimeFormats.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) Para enumerar os formatos com suporte, chame o [**método IMediaParamInfo::GetSupportedTimeFormat.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat)

Para definir o formato de hora, chame [**IMediaParams::SetTimeFormat.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat) Esse método especifica o GUID de formato de hora e os dados *de hora*, que é o número de unidades por tique do relógio. Por exemplo, se o formato de hora for amostras por segundo e os dados de tempo for 32, um valor de carimbo de data/hora de 10 corresponderá a 320 amostras.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



