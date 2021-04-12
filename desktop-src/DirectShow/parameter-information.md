---
description: Informações de Parâmetro
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Informações de Parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500584"
---
# <a name="parameter-information"></a>Informações de Parâmetro

O método [**IMediaParamInfo:: GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) retorna uma estrutura [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) que descreve um parâmetro. Essa estrutura contém as seguintes informações:

-   O membro **mpType** indica o tipo de dados do valor do parâmetro. Para eficiência, todos os parâmetros são implementados como valores de ponto flutuante de 32 bits. A enumeração de [**\_ tipo de MP**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) define se o valor deve ser interpretado como um inteiro, valor de ponto flutuante, booliano ou enumeração (série de inteiros).
-   O membro **mopCaps** indica a quais curvas esse parâmetro dá suporte. Se o tipo de dados for booliano ou enumeração, a única curva à qual o parâmetro pode dar suporte é "Jump".
-   Os membros **mpdMinValue** e **mpdMaxValue** definem os valores mínimo e máximo para esse parâmetro. As curvas para esse parâmetro devem estar dentro desse intervalo.
-   O membro **mpdNeutralValue** é o valor padrão do parâmetro.
-   O membro **szLabel** é o nome do parâmetro e o membro **szUnitText** é o nome da unidade de medida para o parâmetro. Os exemplos podem incluir "volume" e "decibéis" ou "Frequency" e "kHz". Ambas as cadeias de caracteres são em inglês e nunca são localizadas. O DMO pode fornecer versões localizadas por meio do método [**IMediaParamInfo:: GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) .

As informações de cada parâmetro permanecem fixas durante todo o tempo de vida do DMO. Portanto, o cliente pode consultar essas informações uma vez e, em seguida, armazená-las em cache.

**Formatos de hora**

O cliente deve carimbar o tempo dos dados de entrada para que o DMO possa calcular os valores de parâmetro correspondentes. Por padrão, carimbos de data/hora representam unidades de 100 nanossegundos, também chamado de *tempo de referência*. Essa unidade de tempo não é conveniente para todos os aplicativos; no entanto, um DMO tem uma opção para dar suporte a outros formatos de tempo. Os formatos de hora são identificados por GUID.



| **GUID**              | Descrição                   |
|-----------------------|-------------------------------|
| \_referência de tempo de GUID \_ | Hora de referência                |
| hora do GUID \_ \_ música     | Partes por trimestre observação (PPQN) |
| \_exemplos de tempo de GUID \_   | Amostras por segundo            |



 

Os terceiros são incentivados a definir seus próprios formatos de tempo, conforme necessário. No entanto, todos os DMOs devem dar suporte ao tempo de referência. Isso fornece uma linha de base padrão que todos podem usar. Para determinar a quantos formatos de tempo um DMO dá suporte, chame o método [**IMediaParamInfo:: GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) . Para enumerar os formatos com suporte, chame o método [**IMediaParamInfo:: GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) .

Para definir o formato de hora, chame [**IMediaParams:: SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Esse método especifica o GUID de formato de hora e os *dados de hora*, que é o número de unidades por tique de relógio. Por exemplo, se o formato de hora for de exemplos por segundo e os dados de hora forem 32, um valor de carimbo de data/hora 10 corresponde a 320 exemplos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



