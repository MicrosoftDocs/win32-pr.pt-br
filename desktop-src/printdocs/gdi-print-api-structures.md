---
description: Estruturas da API de Impressão GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Estruturas da API de Impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971465"
---
# <a name="gdi-print-api-structures"></a>Estruturas da API de Impressão GDI

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                      | Descrição                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | A [**estrutura de dados DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contém informações sobre a inicialização e o ambiente de uma impressora ou um dispositivo de exibição. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | A [**estrutura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contém os nomes de arquivo de entrada e saída e outras informações usadas pela [**função StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | A [**estrutura DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) define um retângulo a ser criado.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | A [**estrutura \_ CUSTPAPER PSFEATURE**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contém informações sobre um tamanho de papel personalizado para um PostScript driver. Essa estrutura é usada com a função de escape da impressora [**GET \_ PS \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/> |
| [**SAÍDA PSFEATURE \_**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | A [**estrutura PSFEATURE \_ OUTPUT**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contém informações sobre as PostScript de saída do driver. Essa estrutura é usada com a função de escape da impressora [**GET \_ PS \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | A [**estrutura PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) é um header para o buffer de entrada usado com a função de escape da [**impressora POSTSCRIPT \_ INJECTION.**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85))<br/>                                                                            |



 

 

