---
description: Ao usar as caixas de diálogo Windows Microsoft, você deve rotular todos os controles para facilitar a funcionalidade de fala. A caixa de diálogo Executar a seguir mostra um rótulo de controle de texto estático para uma caixa de listagem listada. O texto estático termina com dois-pontos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Nomear controles em caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c33720c08a7f5454b54d7d982b14c091fe6e1df4c18a49cd649f54690f2eb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449819"
---
# <a name="naming-controls-in-dialog-boxes"></a>Nomear controles em caixas de diálogo

Ao usar as caixas de diálogo Windows Microsoft, você deve rotular todos os controles para facilitar a funcionalidade de fala. A caixa **de** diálogo Executar a seguir mostra um rótulo de controle de texto estático para uma caixa de listagem listada. O texto estático termina com dois-pontos.

![captura de tela mostrando a caixa de diálogo Executar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Há dois tipos de controle:

-   Controles que têm suas legendas como uma propriedade desse controle, como botões de comando e caixas de seleção. Os auxiliares de acessibilidade não têm problemas para identificar esses controles, desde que a legenda seja definida corretamente.
-   Os controles que não têm suas próprias legendas, como controles de edição, caixas de listagem e exibições de lista, devem ser rotulados usando controles de texto estático separados. Para obter mais informações sobre controles que não têm suas próprias legendas, consulte [Controls Without Caption Properties](controls-without-caption-properties.md).

Várias técnicas podem ser usadas para superar situações em que os controles não têm suas próprias legendas, mas só são eficazes para janelas exibidas pelo SDM (Gerenciador de Diálogo Standard). Todas as outras janelas precisam expor os nomes e a relação entre controles dando suporte explícito Microsoft Active Accessibility. Para obter mais informações Acessibilidade Ativa, consulte a [seção Acessibilidade](/windows/desktop/accessibility) do Biblioteca MSDN.

 

 
