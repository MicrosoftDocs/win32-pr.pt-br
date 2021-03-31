---
title: Constantes e enumerações do DWM
description: Esta seção contém informações sobre as constantes e enumerações usadas nas APIs do Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), constantes
- DWM (Gerenciador de Janelas da Área de Trabalho), constantes
- Gerenciador de Janelas da Área de Trabalho (DWM), enumerações
- DWM (Gerenciador de Janelas da Área de Trabalho), enumerações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636130"
---
# <a name="dwm-constants-and-enumerations"></a>Constantes e enumerações do DWM

Esta seção contém informações sobre as constantes e enumerações usadas nas APIs do Gerenciador de Janelas da Área de Trabalho (DWM).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Desfoque de DWM por trás de constantes**](dwm-bb-constants.md)<br/>                          | Sinalizadores usados pela estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar quais dos seus membros contêm informações válidas.<br/>                                                                    |
| [**Constantes de composição do DWM Enable**](dwm-ec-constants.md)<br/>                   | Sinalizadores usados pela função [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  para alterar o estado da composição do DWM.<br/>                                                                             |
| [**\_amostragem do \_ quadro de origem do DWM \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | Sinalizadores usados pela função [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) para especificar o tipo de amostragem de quadro.<br/>                                                                            |
| [**\_requisitos da \_ janela da guia DWM \_**](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | Retornado por DwmGetUnmetTabRequirements para indicar os requisitos necessários para uma janela colocar guias na barra de título do aplicativo.<br/>                                                                    |
| [**Constantes do DWM \_ TNP**](dwm-tnp-constants.md)<br/>                                | Sinalizadores usados pela estrutura [**de \_ \_ Propriedades de miniatura do DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) para indicar quais dos seus membros contêm informações válidas.<br/>                                               |
| [**DWMFLIP3DWINDOWPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | Sinalizadores usados pela função [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar a política de janela Flip3D.<br/>                                                                               |
| [**DWMNCRENDERINGPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | Sinalizadores usados pela função [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar a política de renderização de área não cliente.<br/>                                                                   |
| [**DWMTRANSITION \_ OWNEDWINDOW \_ target**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | Identifica o destino.<br/>                                                                                                                                                                               |
| [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | Sinalizadores usados pelas funções [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar atributos de janela para renderização não cliente.<br/> |
| [**tipo de gesto \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | Identifica o tipo de gesto especificado em [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).<br/>                                                                                                               |



 

 

 





