---
title: Funções básicas para uso em um contexto de dispositivo
description: As funções WCS a seguir oferecem funcionalidades básicas de mapeamento de cores em contextos de dispositivo. Eles são úteis para todos os aplicativos que precisam implementar o gerenciamento de cores com baixa sobrecarga e intervenção mínima do usuário.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Sistema de Cores (WCS), funções
- WCS (Windows color system),funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- colors,functions
- Referência do WCS, funções
- referência para WCS, funções
- Windows Sistema de Cores (WCS), contextos de dispositivo
- WCS (Windows color system), contextos de dispositivo
- gerenciamento de cores de imagem, contextos de dispositivo
- gerenciamento de cores, contextos de dispositivo
- cores, contextos de dispositivo
- Referência do WCS, contextos de dispositivo
- referência para WCS, contextos de dispositivo
- contextos de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210975"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Funções básicas para uso em um contexto de dispositivo

As funções WCS a seguir oferecem funcionalidades básicas [de mapeamento de](c.md) cores em contextos de dispositivo. Eles são úteis para todos os aplicativos que precisam implementar o gerenciamento de cores com baixa sobrecarga e intervenção mínima do usuário.



| Função                                                           | Descrição                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Verifica se as cores fornecidas estão na gama de um dispositivo.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corrige as entradas em uma paleta para um contexto de dispositivo.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Executa o mapeamento de cores para fins de visualização.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Cria um espaço de cores.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Exclui um espaço de cores.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Enumera os perfis de cor de saída disponíveis para um determinado contexto de dispositivo.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Função de retorno de chamada definida pelo aplicativo [**para EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). O nome dessa função também é definido pelo aplicativo. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtém o espaço de cor de entrada atual em um contexto de dispositivo. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Obtém o perfil de cor de saída atual de um contexto de dispositivo.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Obtém a [**estrutura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de um contexto de dispositivo.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Define o espaço de cor de entrada de um contexto de dispositivo.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Liga ou desliga o gerenciamento de cores em um contexto de dispositivo.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Define o perfil de cor de saída para um determinado contexto de dispositivo.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumera todos os perfis de cores que atendem aos critérios de enumeração no escopo de gerenciamento de perfil especificado.                                      |



 

 

 




