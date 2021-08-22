---
title: Funções de calibragem e caracterização de dispositivo
description: As funções a seguir são úteis para escrever ferramentas de calibragem e ajustes de dispositivo necessárias para instalar e calibrar dispositivos de exibição de cores, como monitores e impressoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Sistema de Cores (WCS), funções
- WCS (Windows color system),funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- colors,functions
- Referência do WCS, funções
- referência para WCS, funções
- Windows Sistema de Cores (WCS), calibragem do dispositivo
- WCS (Windows color system), calibragem do dispositivo
- gerenciamento de cores da imagem, calibragem do dispositivo
- gerenciamento de cores, calibragem do dispositivo
- cores, calibragem do dispositivo
- Referência do WCS, calibragem de dispositivo
- referência para WCS, calibragem de dispositivo
- Windows Sistema de Cores (WCS), seta
- WCS (Windows color system),ole
- gerenciamento de cores da imagem, cteres
- gerenciamento de cores, cteres
- colors, colors
- Referência do WCS, ole
- referência para WCS, ole
- calibragem de dispositivo
- Calibração
- Caracterização
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aea24f0a1e033df62c70674c44c9b5e9c6c0e0de1011b9ea95b9e5389d6004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452017"
---
# <a name="device-calibration-and-characterization-functions"></a>Funções de calibragem e caracterização de dispositivo

As funções a seguir são úteis para escrever ferramentas de calibragem e ajustes de dispositivo necessárias para instalar e calibrar dispositivos de exibição de cores, como monitores e impressoras.



| Função | Descrição |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Fecha um alça de perfil aberto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Cria um perfil de *link* de dispositivo do ICC (International Color Consortium) de um conjunto de perfis de cores, usando as intenções especificadas. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia dados de um elemento de perfil marcado especificado de um perfil de cor especificado em um buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera o nome da marca especificado por *dwIndex* na tabela de marca de um determinado perfil de cor do ICC (International Color Consortium), em que *dwIndex* é um índice de base única nessa tabela. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera o conteúdo do perfil de cor dado um alça para um perfil de cor aberto.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera ou deriva a estrutura de título ICC do perfil de cor ICC ou do perfil XML do WCS. Drivers e aplicativos devem assumir que **retornar TRUE** indica apenas que um header estruturado corretamente é retornado. Cada marca ainda precisará ser validada independentemente usando APIs ICM2 herdadas ou APIs de esquema XML. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera o número de elementos marcados em um determinado perfil de cor. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera o dicionário PostScript renderização de cores nível 2 do perfil de cor ICC especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera a intenção de renderização de cores PostScript Nível 2 [de um](r.md) perfil de cor ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera a matriz PostScript de espaço de [cor](c.md) nível 2 de um perfil de cor ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Informa se uma marca ICC (International Color Consortium) especificada está presente no perfil de cor especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite que você determine se o perfil especificado é um perfil válido do ICC (International Color Consortium) ou um handle de perfil válido do WCS (Sistema de Cores do Windows) que pode ser usado para o gerenciamento de cores. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Cria um alça para um perfil de cor especificado. O handle pode ser usado em outras funções de gerenciamento de perfil. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Define os dados do elemento para um elemento de perfil marcado em um perfil de cor ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Cria em um perfil de cor ICC especificado uma nova marca que faz referência aos mesmos dados de uma marca existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Define o tamanho de um elemento marcado em um perfil de cor ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Define os dados de header em um perfil de cor ICC especificado. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina se o gerenciamento do sistema do estado de calibragem de exibição está habilitado. |



 

 

 




