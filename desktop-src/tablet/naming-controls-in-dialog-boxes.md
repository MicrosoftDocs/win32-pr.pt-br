---
description: Ao usar as caixas de diálogo do Microsoft Windows, você deve rotular todos os controles para facilitar a funcionalidade de fala. A caixa de diálogo Executar seguinte mostra um rótulo de controle de texto estático para uma caixa de listagem suspensa. O texto estático termina com dois-pontos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Controles de nomenclatura em caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570207"
---
# <a name="naming-controls-in-dialog-boxes"></a>Controles de nomenclatura em caixas de diálogo

Ao usar as caixas de diálogo do Microsoft Windows, você deve rotular todos os controles para facilitar a funcionalidade de fala. A caixa de diálogo **executar** seguinte mostra um rótulo de controle de texto estático para uma caixa de listagem suspensa. O texto estático termina com dois-pontos.

![captura de tela mostrando a caixa de diálogo Executar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Há dois tipos de controle:

-   Controles que têm suas legendas como uma propriedade desse controle, como botões de comando e caixas de seleção. Os recursos de acessibilidade não têm problemas para identificar esses controles, desde que a legenda esteja definida corretamente.
-   Controles que não têm suas próprias legendas, como controles de edição, caixas de listagem e exibições de lista, devem ser rotulados usando controles de texto estáticos separados. Para obter mais informações sobre controles que não têm suas próprias legendas, consulte [controles sem propriedades de legenda](controls-without-caption-properties.md).

Várias técnicas podem ser usadas para superar situações nas quais os controles não têm suas próprias legendas, mas são apenas eficazes para janelas que são exibidas pelo SDM (Gerenciador de caixas de diálogo padrão). Todas as outras janelas precisam expor os nomes e a relação entre os controles com suporte explícito ao Microsoft Acessibilidade Ativa. Para obter mais informações sobre Acessibilidade Ativa, consulte a seção [acessibilidade](/windows/desktop/accessibility) da biblioteca MSDN.

 

 
