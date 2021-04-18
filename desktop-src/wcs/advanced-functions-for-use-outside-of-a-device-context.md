---
title: Funções avançadas para uso fora de um contexto de dispositivo
description: Essas funções fornecem recursos avançados de gerenciamento de cores fora dos contextos de dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105764341"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funções avançadas para uso fora de um contexto de dispositivo

Essas funções fornecem recursos avançados de gerenciamento de cores fora dos contextos de dispositivo.



| Função                                                           | Descrição                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (ou **ApplyCallbackFunction**) é uma função de retorno de chamada que você implementa que atualiza os dados de configuração do WCS enquanto a caixa de diálogo exibida pela função [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) está em execução. |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Verifica se os pixels em um bitmap especificado estão dentro da [gama](g.md) de saída de uma transformação especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se as cores em uma matriz ficam dentro da [gama](g.md) de saída de uma transformação especificada. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte nomes de cores em um espaço de cores nomeado para indexar números em um perfil de cores ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Aceita uma matriz de perfis ou um único [perfil de link de dispositivo](d.md) e cria uma transformação de cor que os aplicativos podem usar para executar o mapeamento de cores. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Exclui uma determinada transformação de cor. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera várias informações sobre o módulo de gerenciamento de cores (CMM) que criou a transformação de cor especificada. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera informações sobre o perfil de cor do consórcio de cor internacional (ICC) que é especificado no primeiro parâmetro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Função de retorno de chamada fornecida pelo aplicativo para relatar o progresso. O nome dessa função também é definido pelo aplicativo.                                                 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite que você selecione o módulo de gerenciamento de cores preferencial (CMM) a ser usado. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Fornece controle de usuário sobre o gerenciamento de cores por meio de uma caixa de diálogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Converte cores de bitmap usando uma transformação de cor.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Traduz uma matriz de cores do [espaço de cor](c.md) de origem para o espaço de cores de destino, conforme definido por uma transformação de cor. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina se as cores em uma matriz estão dentro da gama de saída de uma transformação de cor WCS especificada.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Traduz uma matriz de cores do espaço de cor de origem para o espaço de cores de destino, conforme definido por uma transformação de cor.                                                |



 

 

 




