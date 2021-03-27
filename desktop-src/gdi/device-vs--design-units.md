---
description: Um aplicativo pode recuperar as métricas de fonte para uma fonte física somente depois que a fonte tiver sido selecionada em um contexto de dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo versus unidades de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827660"
---
# <a name="device-vs-design-units"></a>Dispositivo versus unidades de design

Um aplicativo pode recuperar as métricas de fonte para uma fonte física somente depois que a fonte tiver sido selecionada em um contexto de dispositivo. Quando uma fonte é selecionada em um contexto de dispositivo, ela é dimensionada para o dispositivo. As métricas de fonte específicas para o dispositivo são conhecidas como unidades de dispositivo.

As métricas portáteis em fontes são conhecidas como unidades de design. Para aplicar a um dispositivo especificado, as unidades de design devem ser convertidas em unidades de dispositivo. Use a fórmula a seguir para converter unidades de design em unidades de dispositivo.

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*Points*/72) \* *DeviceResolution*

As variáveis nesta fórmula têm os seguintes significados.



| Variável           | Descrição                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | Especifica a métrica de fonte *DesignUnits* convertida em unidades de dispositivo. Esse valor está nas mesmas unidades que o valor especificado para *DeviceResolution*.                          |
| *DesignUnits*      | Especifica a métrica de fonte a ser convertida em unidades de dispositivo. Esse valor pode ser qualquer métrica de fonte, incluindo a largura de um caractere ou o valor mais ascendente para uma fonte inteira. |
| *unitsPerEm*       | Especifica o tamanho quadrado em para a fonte.                                                                                                                                 |
| *Pontos*        | Especifica o tamanho da fonte, em pontos. (Um ponto é igual a 1/72 de uma polegada.)                                                                                                 |
| *DeviceResolution* | Especifica o número de unidades de dispositivo (pixels) por polegada. Os valores típicos podem ser 300 para uma impressora laser ou 96 para uma tela VGA.                                                |



 

Esta fórmula não deve ser usada para converter unidades de dispositivo de volta em unidades de design. As unidades de dispositivo são sempre arredondadas para o pixel mais próximo. O erro de arredondamento propagado pode se tornar muito grande, especialmente quando um aplicativo está trabalhando com tamanhos de tela.

Para solicitar unidades de design, crie uma fonte lógica cuja altura seja especificada como *unitsPerEm*. Os aplicativos podem recuperar o valor de *unitsPerEm* chamando a função [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) e verificando o membro **ntmSizeEM** da estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .

 

 



