---
title: 'sRGB: um espaço de cores padrão'
description: Como resultado das considerações sobre largura de banda da Internet, a Hewlett-Packard e a Microsoft proempção de um espaço de cores predefinido padrão conhecido como sRGB (IEC 61966-2-1), de modo a permitir mapeamento de cores preciso com pouca sobrecarga de dados.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- WCS (Sistema de Cores do Windows), espaço de cor sRGB
- WCS (Sistema de Cores do Windows), espaço de cor sRGB
- gerenciamento de cores da imagem, espaço de cor sRGB
- gerenciamento de cores, espaço de cor sRGB
- colors,sRGB color space
- Espaço de cor sRGB
- espaços de cores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443637"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: um espaço de cor padrão

Como resultado das considerações sobre largura de banda da Internet, o [](c.md) Hewlett-Packard e a Microsoft proempção de um espaço de cores predefinido padrão [](c.md) conhecido como *sRGB* (IEC 61966-2-1), de modo a permitir o mapeamento de cores preciso com muito pouca sobrecarga de dados.

Uma versão do arquivo de ajuda de um white paper que discute os detalhes técnicos de sRGB, sRGB.hlp, está disponível na pasta Ajuda da Referência do Programador do \\ WCS 1.0.

Formatos de arquivo diferentes podem usar ou adicionar um sinalizador para especificar que a imagem está no espaço de cores sRGB. No formato DIB (bitmap independente de dispositivo) do Windows, definir o membro **bV5CSType** da estrutura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) como **\_ LCS sRGB** especifica que as cores DIB estão no espaço de cores sRGB.

O WCS 1.0 fornece suporte nativo para sRGB. Há duas maneiras de usar o WCS 1.0 para renderizar uma imagem definida no espaço de cores sRGB:

**Para renderizar uma imagem dentro do contexto do dispositivo**

1.  Crie um DC (contexto de dispositivo) no dispositivo de exibição.
2.  Definir o gerenciamento de cores usando [**a função SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)
3.  Use a [**função SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir o DIB para o DC. Desde que o membro **bV5CSMType** da estrutura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) de DIBs seja definido como **LCS \_ sRGB,** o sistema executará o gerenciamento de cores apropriado.

**Para renderizar uma imagem fora do contexto do dispositivo**

1.  Crie uma transformação usando [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw) O **membro lcsCSType** da estrutura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) apontada pelo parâmetro *pLogColorSpace* deve ser definido como **LCS \_ sRGB.** O *parâmetro hDestProfile* indica o espaço de cores do dispositivo de exibição.
2.  Use a transformação de cor criada para corresponder à imagem antes de exibi-la no dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Padrões do WCS 1.0 para espaço de cor de entrada e perfil de saída

Quando nenhum espaço de cor de entrada é especificado, por padrão, o WCS 1.0 usa o espaço de cores sRGB como o espaço de cor de entrada para mapeamento [de cores.](c.md)

Quando nenhum perfil de saída é especificado, mas um dispositivo padrão é especificado, o WCS 1.0 seleciona um perfil de saída padrão. Se o dispositivo padrão não tiver um perfil associado, o WCS 1.0 usará o espaço de cores sRGB como o perfil de saída.

A tabela a seguir mostra as transformaçãos de cor resultantes quando um dispositivo padrão não está disponível.



|  &nbsp;                               | Perfil de saída especificado                              | Perfil de saída não especificado                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Espaço de cor de entrada especificado     | A transformação usa os perfis especificados.                | A transformação converte do espaço de cor de entrada conhecido em sRGB. |
| Espaço de cor de entrada não especificado | Transforme as conversões de sRGB em perfil de saída conhecido. | A transformação de sRGB para sRGB é assumida; nada é feito. |



 

## <a name="srgb-and-embedded-profiles"></a>Perfis sRGB e inseridos

A partir da versão 2.0 do ICM, os aplicativos que utilizam o WCS podem inserir perfis em imagens. Os perfis inseridos auxiliam os aplicativos dos usuários a manter uma aparência de cor consistente, mesmo que as imagens sejam transmitidas pela Internet.

As imagens que usam o espaço de cores sRGB não precisam de um perfil de cor inserido. Como eles não têm perfil inserido, as imagens baseadas em sRGB são menores e facilmente transferíveis entre canais de dados com largura de banda limitada.

Os aplicativos devem definir o sinalizador **\_ SRGB** do LCS no header de bitmap da imagem para indicar que a imagem usa o espaço de cor sRGB. Para obter detalhes, consulte [Estruturas de header do Bitmap do Windows](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 