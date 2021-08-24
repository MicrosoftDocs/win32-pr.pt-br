---
description: Mensagens de qualidade
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensagens de qualidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747696"
---
# <a name="quality-messages"></a>Mensagens de qualidade

As mensagens de qualidade são definidas com [**a estrutura Quality.**](/windows/win32/api/strmif/ns-strmif-quality) Essa estrutura contém os seguintes membros:

-   **Digite:** Definido pela [**enumeração QualityMessageType;**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) Seja Em Caso de Desastre, indicando que o filtro está recebendo dados muito pequenos ou Inundação, indicando que o filtro está recebendo muitos dados.
-   **Proporção:** O ajuste solicitado na taxa de dados, de uma linha de base de 1000. Por exemplo, 750 indica 75% e 1500 indica 150%.
-   **Tardia:** Tempo de referência que indica a hora em que a amostra mais recente chegou. O valor será negativo se a amostra chegar mais cedo.
-   **TimeStamp:** O carimbo de data/hora no exemplo mais recente.

Por exemplo, suponha que um exemplo com um carimbo de data/hora de 240 milissegundos (ms) atinja o renderador a 280 ms, hora do fluxo. O renderador cria uma mensagem de qualidade do tipo Desmistência. O exemplo chegou com 40 ms de atraso, portanto, o **membro Late** é 400000. (Todos os tempos de referência estão em unidades de 100 nanossegundos.) O **membro TimeStamp** é 2400000.

Para o **membro Proportion,** o renderador pode usar uma média em execução para calcular o valor. Talvez os exemplos tenham sido chegando a tempo e essa amostra seja uma anomalia. Nesse caso, o renderador pode solicitar apenas uma pequena correção. Por outro lado, se os exemplos atrasarem consistentemente, o renderador poderá solicitar uma correção maior.

O controle de qualidade é tratado por meio da interface [**IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) Ele contém dois métodos.

-   [**Notificar**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envia uma mensagem de qualidade.
-   [**SetSink:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)especifica um gerenciador de qualidade personalizado.

Um objeto que implementa **IQualityControl** recebe mensagens de qualidade por meio de seu **método Notify.** Ele pode manipular a mensagem ou passar a mensagem para outro objeto. Se o aplicativo chamar o método **SetSink** do objeto, o objeto deverá delegar o controle de qualidade ao gerenciador de qualidade especificado.

 

 



