---
title: Data e hora de efetivação
description: Data e hora de efetivação é uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos de informações para algum momento no futuro, quando a alteração tem uma alta probabilidade de ser totalmente replicada.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004934"
---
# <a name="effective-date-and-time"></a>Data e hora de efetivação

*Data e hora de efetivação* é uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos de informações para algum momento no futuro, quando a alteração tem uma alta probabilidade de ser totalmente replicada. Para implementar datas efetivas, os objetos de aplicativo devem incluir um carimbo de data/hora de efetivação, que é preenchido quando o objeto é criado ou alterado. Os consumidores dos objetos verificam o carimbo de data/hora e adiam o uso dos objetos até que essa data e hora sejam atingidas.

Algumas considerações importantes:

-   Os aplicativos que escolhem essa abordagem devem garantir que haja um conjunto de dados aplicáveis a serem usados até que os objetos atualizados se tornem efetivos.
-   O serviço de tempo distribuído no Windows NT 4,0 mantém os relógios da sincronização do Windows 2000 conectada. No entanto, nenhum serviço de tempo é perfeito; portanto, há uma pequena janela para distorção de versão.
-   Definir uma boa data de efetivação pressupõe o conhecimento da latência geral de replicação para o sistema distribuído em questão. Em uma rede estável, uma boa regra prática para datas efetivas é a (hora da atualização) + (2 \* (latência geral média)). Portanto, para um sistema cuja média de latência geral é de 4 horas, um atraso de 8 horas é razoável.
-   Em uma rede instável, a determinação de um valor "bom" para datas efetivas é muito mais difícil, pois a latência pode ser altamente variável. A data de efetivação é a mais "eficaz" em uma rede instável quando combinada com outras estratégias de prevenção ou detecção, como somas de verificação ou GUIDs de consistência. Para obter mais informações, consulte [somas de verificação e contagens de objetos](checksums-and-object-counts.md).

 

 




