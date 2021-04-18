---
title: Funções de WCS para CMMs (módulos de gerenciamento de cores) a serem implementadas
description: As funções a seguir devem ser implementadas por CMMs (módulos de gerenciamento de cores) e exportadas para que o sistema operacional chame.
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- WCS (sistema de cores do Windows), módulo de gerenciamento de cores (CMM)
- WCS (sistema de cores do Windows), módulo de gerenciamento de cores (CMM)
- gerenciamento de cores de imagem, módulo de gerenciamento de cores (CMM)
- gerenciamento de cores, módulo de gerenciamento de cores (CMM)
- cores, módulo de gerenciamento de cores (CMM)
- Referência do WCS, módulo de gerenciamento de cores (CMM)
- referência para WCS, módulo de gerenciamento de cores (CMM)
- Módulo de gerenciamento de cores (CMM)
- CMM (módulo de gerenciamento de cores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105795510"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>Funções de WCS para CMMs (módulos de gerenciamento de cores) a serem implementadas

As funções a seguir devem ser implementadas por CMMs (módulos de gerenciamento de cores) e exportadas para que o sistema operacional chame.



| Função                                                                     | Descrição                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina se as cores determinadas estão dentro da [gama](./g.md) de saída de uma transformação especificada. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina se as corridas de RGB especificadas ficam na [gama](./g.md) de saída de uma transformação especificada. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                           | Verifica as cores de bitmap em uma gama de saída.                                             |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Converte nomes de cores em um espaço de cores nomeado para indexar números em um perfil de cor |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Cria um [perfil de link de dispositivo](./d.md) no formato especificado pelo consórcio de cor internacional em sua especificação de formato de perfil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Aceita uma matriz de perfis ou um único [perfil de link de dispositivo](./d.md) e cria uma transformação de cor. Essa transformação é um mapeamento do espaço de cores especificado pelo primeiro perfil para o do segundo perfil e assim por diante para o último. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Cria um perfil de cor de exibição de uma estrutura [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Cria um perfil de cor de exibição de uma estrutura [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Preterido. Não há uma API de substituição porque esta não estava mais sendo usada. Os desenvolvedores de módulos do CMM alternativos não são necessários para implementá-lo. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Cria uma transformação de cor que mapeia de um [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) de entrada para um espaço de destino opcional e, em seguida, para um dispositivo de saída, usando um conjunto de sinalizadores que definem como a transformação deve ser criada. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Cria uma transformação de cor que mapeia de um [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) de entrada para um espaço de destino opcional e, em seguida, para um dispositivo de saída, usando um conjunto de sinalizadores que definem como a transformação deve ser criada. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Preterido. Não há uma API de substituição porque esta não estava mais sendo usada. Os desenvolvedores de módulos do CMM alternativos não são necessários para implementá-lo. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Exclui uma transformação de cor especificada e libera qualquer memória associada a ela. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera várias informações sobre o módulo de gerenciamento de cores (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera informações sobre o perfil de cor nomeada especificado. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | Obtém um dicionário de renderização de cor PostScript.                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera a [tentativa de renderização](rendering-intents.md) de cor PostScript Nível 2 de um perfil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | Obtém uma matriz de espaço de cores PostScript.                                                      |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Relata se o perfil fornecido é um perfil ICC válido que pode ser usado para o gerenciamento de cores. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Traduz uma matriz de cores de um [espaço de cor](rendering-intents.md) de origem para um espaço de cores de destino usando uma transformação de cor. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Traduz um RGBQuad fornecido pelo aplicativo no [espaço de cores](color-spaces.md)do dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Traduz um bitmap de um espaço de [cor](color-spaces.md) para outro usando uma transformação de cor. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Converte um bitmap de um formato definido em um formato definido diferente e chama periodicamente uma função de retorno de chamada, se um for especificado, para relatar o progresso e permitir que o aplicativo de chamada encerre a tradução. |



 

 

 