---
description: Estruturas da API de impressão GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Estruturas da API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ae427af0112061e6b90afa71cc2b65427d477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759854"
---
# <a name="gdi-print-api-structures"></a>Estruturas da API de impressão GDI

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                      | Descrição                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | A estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contém informações sobre a inicialização e o ambiente de uma impressora ou um dispositivo de vídeo. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | A estrutura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contém os nomes de arquivo de entrada e saída e outras informações usadas pela função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | A estrutura [**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) define um retângulo a ser criado.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | A estrutura [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contém informações sobre um tamanho de papel personalizado para um driver PostScript. Essa estrutura é usada com a função de escape obter a impressora [**\_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) .<br/> |
| [**saída de PSFEATURE \_**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | A estrutura de [**\_ saída PSFEATURE**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contém informações sobre opções de saída do driver PostScript. Essa estrutura é usada com a função de escape obter a impressora [**\_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) .<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | A estrutura [**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) é um cabeçalho para o buffer de entrada usado com a função de escape de impressora de [**\_ injeção de PostScript**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)) .<br/>                                                                            |



 

 

