---
title: 'sRGB: um espaço de cores padrão'
description: Como resultado de considerações sobre largura de banda da Internet, a Hewlett-Packard e a Microsoft propuseram a adoção de um espaço de cores predefinido padrão conhecido como sRGB (IEC 61966-2-1), para permitir o mapeamento preciso de cores com muito pouca sobrecarga de dados.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Sistema de cores (WCS), espaço de cores sRGB
- WCS (Windows sistema de cores), espaço de cores sRGB
- gerenciamento de cores de imagem, espaço de cores sRGB
- gerenciamento de cores, espaço de cores sRGB
- cores, espaço de cores sRGB
- espaço de cores sRGB
- espaços de cores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0779ec79868a6ec6d78e447b7ee3473847b8fdc1ffa165897abd2dcbcb7a0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965915"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: um espaço de cores padrão

Como resultado de considerações sobre largura de banda da Internet, a Hewlett-Packard e a Microsoft propuseram a adoção de um [espaço de cores](c.md) predefinido padrão conhecido como *sRGB* (IEC 61966-2-1), para permitir o mapeamento preciso de [cores](c.md) com muito pouca sobrecarga de dados.

Uma versão de arquivo de ajuda de um white paper discutindo os detalhes técnicos do sRGB, sRGB. hlp, está disponível na \\ pasta de ajuda da referência do programador do WCS 1,0.

Formatos de arquivo diferentes podem usar ou adicionar um sinalizador para especificar que a imagem está no espaço de cores sRGB. no formato DIB (bitmap independente de dispositivo) Windows, definir o membro **bV5CSType** da estrutura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) para **LCS \_ sRGB** especifica que as cores de DIB estão no espaço de cores sRGB.

O WCS 1,0 fornece suporte nativo para sRGB. Há duas maneiras de usar o WCS 1,0 para renderizar uma imagem definida no espaço de cores sRGB:

**Para renderizar uma imagem dentro do contexto do dispositivo**

1.  Crie um DC (contexto de dispositivo) no dispositivo de vídeo.
2.  Defina o gerenciamento de cores usando a função [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .
3.  Use a função [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir o DIB para o controlador de domínio. Desde que o membro **bV5CSMType** da estrutura de Dibs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) seja definido como **LCS \_ sRGB**, o sistema executará o gerenciamento de cores apropriado.

**Para renderizar uma imagem fora do contexto do dispositivo**

1.  Crie uma transformação usando [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw). O membro **lcsCSType** da estrutura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) apontada pelo parâmetro *PLogColorSpace* deve ser definido como **LCS \_ sRGB**. O parâmetro *hDestProfile* indica o espaço de cores do dispositivo de vídeo.
2.  Use a transformação de cor criada para corresponder à cor da imagem antes de exibi-la no dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Padrões WCS 1,0 para o espaço de cor de entrada e o perfil de saída

Quando nenhum espaço de cor de entrada é especificado, por padrão, o WCS 1,0 usa o espaço de cores sRGB como o espaço de cor de entrada para o [mapeamento de cores](c.md).

Quando nenhum perfil de saída é especificado, mas um dispositivo padrão é especificado, o WCS 1,0 seleciona um perfil de saída padrão. Se o dispositivo padrão não tiver um perfil associado, o WCS 1,0 usará o espaço de cores sRGB como o perfil de saída.

A tabela a seguir mostra as transformações de cor resultantes quando um dispositivo padrão não está disponível.



|  &nbsp;                               | Perfil de saída especificado                              | Perfil de saída não especificado                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Espaço de cores de entrada especificado     | A transformação usa os perfis especificados.                | A transformação converte o espaço de cor de entrada conhecido em sRGB. |
| Espaço de cores de entrada não especificado | A transformação converte de sRGB para perfil de saída conhecido. | A transformação de sRGB para sRGB é assumida; Nada é feito. |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB e perfis inseridos

a partir do ICM versão 2,0, os aplicativos que utilizam o WCS podem inserir perfis em imagens. Os perfis incorporados ajudam os aplicativos dos usuários a manter uma aparência de cor consistente, mesmo que as imagens sejam transmitidas pela Internet.

Imagens que usam o espaço de cores sRGB não precisam de um perfil de cor inserido. Como não têm nenhum perfil inserido, as imagens baseadas em sRGB são menores e mais prontamente transferíveis em canais de dados com largura de banda limitada.

Os aplicativos devem definir o sinalizador **LCS \_ sRGB** no cabeçalho de bitmap da imagem para indicar que a imagem usa o espaço de cores sRGB. para obter detalhes, consulte [Windows estruturas de cabeçalho de Bitmap](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 