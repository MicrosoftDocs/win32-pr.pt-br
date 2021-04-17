---
title: Funções de calibragem e caracterização de dispositivo
description: As funções a seguir são úteis para a gravação de ferramentas de calibragem de dispositivo e de caracterização necessárias para instalar e calibrar dispositivos de exibição de cor, como monitores e impressoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- WCS (sistema de cores do Windows), funções
- WCS (sistema de cores do Windows), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- WCS (sistema de cores do Windows), calibragem do dispositivo
- WCS (sistema de cores do Windows), calibragem do dispositivo
- gerenciamento de cores de imagem, calibragem de dispositivo
- gerenciamento de cores, calibragem do dispositivo
- cores, calibragem do dispositivo
- Referência do WCS, calibragem do dispositivo
- referência para WCS, calibragem de dispositivo
- WCS (sistema de cores do Windows), caracterização
- WCS (sistema de cores do Windows), caracterização
- gerenciamento de cores de imagem, caracterização
- gerenciamento de cores, caracterização
- cores, caracterização
- Referência do WCS, caracterização
- referência para WCS, caracterization
- calibragem do dispositivo
- calibragem
- caracterização
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105762246"
---
# <a name="device-calibration-and-characterization-functions"></a>Funções de calibragem e caracterização de dispositivo

As funções a seguir são úteis para a gravação de ferramentas de calibragem de dispositivo e de caracterização necessárias para instalar e calibrar dispositivos de exibição de cor, como monitores e impressoras.



| Função | Descrição |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Fecha um identificador de perfil aberto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Cria um *perfil de link de dispositivo* do consórcio de cor internacional (ICC) a partir de um conjunto de perfis de cor, usando as tentativas especificadas. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia dados de um elemento de perfil marcado especificado de um perfil de cor especificado em um buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera o nome de marca especificado por *dwIndex* na tabela de marcas de um perfil de cor ICC (International Color Consortium) específico, em que *dwIndex* é um índice de base um para essa tabela. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera o conteúdo do perfil de cor dado um identificador para um perfil de cor aberta.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera ou deriva a estrutura de cabeçalho ICC do perfil de cor ICC ou do perfil XML WCS. Os drivers e os aplicativos devem assumir que retornar **true** apenas indica que um cabeçalho estruturado corretamente é retornado. Cada marca ainda precisará ser validada de forma independente, usando APIs ICM2 herdadas ou APIs de esquema XML. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera o número de elementos marcados em um determinado perfil de cor. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera o dicionário de renderização de cor PostScript Nível 2 do perfil de cor ICC especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera a [tentativa de renderização](r.md) de cor PostScript Nível 2 de um perfil de cor ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera a matriz de espaço de [cores](c.md) de nível 2 PostScript de um perfil de cor ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Relata se uma marca especificada do consórcio de cor internacional (ICC) está presente no perfil de cor especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite que você determine se o perfil especificado é um perfil ICC (International Color Consortium) válido ou um identificador de perfil válido do WCS (sistema de cores do Windows) que pode ser usado para o gerenciamento de cores. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Cria um identificador para um perfil de cor especificado. O identificador pode então ser usado em outras funções de gerenciamento de perfil. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Define os dados do elemento para um elemento de perfil marcado em um perfil de cor ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Cria em um perfil de cor ICC especificado uma nova marca que faz referência aos mesmos dados de uma marca existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Define o tamanho de um elemento marcado em um perfil de cor ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Define os dados de cabeçalho em um perfil de cor ICC especificado. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado. |



 

 

 




