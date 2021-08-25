---
title: Funções avançadas para uso fora de um contexto de dispositivo
description: Essas funções fornecem recursos avançados de gerenciamento de cores fora dos contextos do dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Sistema de Cores (WCS), funções
- WCS (Windows Color System), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- colors,functions
- Referência do WCS, funções
- referência para WCS, funções
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814607"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funções avançadas para uso fora de um contexto de dispositivo

Essas funções fornecem recursos avançados de gerenciamento de cores fora dos contextos do dispositivo.



| Função                                                           | Descrição                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (ou **ApplyCallbackFunction**) é uma função de retorno de chamada que você implementa que atualiza os dados de configuração do WCS enquanto a caixa de diálogo exibida pela [**função SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) está em execução. |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Verifica se os pixels em um bitmap especificado estão dentro da gama de [saída](g.md) de uma transformação especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se as cores em uma matriz estão dentro da gama [de saída](g.md) de uma transformação especificada. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte nomes de cores em um espaço de cores nomeado em números de índice em um perfil de cor do ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma índices em um espaço de cores em uma matriz de nomes em um espaço de cores nomeado. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Aceita uma matriz de perfis ou um único perfil de link de [dispositivo](d.md) e cria uma transformação de cor que os aplicativos podem usar para executar o mapeamento de cores. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Exclui uma transformação de cor determinada. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera várias informações sobre o CMM (módulo de gerenciamento de cores) que criou a transformação de cor especificada. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera informações sobre o perfil de cor nomeado do ICC (International Color Consortium) especificado no primeiro parâmetro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Função de retorno de chamada fornecida pelo aplicativo para relatar o progresso. O nome dessa função também é definido pelo aplicativo.                                                 |
| [**SelecioneCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite que você selecione o CMM (módulo de gerenciamento de cores) preferencial a ser usado. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Fornece controle do usuário sobre o gerenciamento de cores por meio de uma caixa de diálogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Converte cores de bitmap usando uma transformação de cor.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte uma matriz de cores do espaço de cores de [origem](c.md) para o espaço de cores de destino, conforme definido por uma transformação de cor. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina se as cores em uma matriz estão dentro da gama de saída de uma transformação de cor WCS especificada.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte uma matriz de cores do espaço de cores de origem para o espaço de cores de destino, conforme definido por uma transformação de cor.                                                |



 

 

 




