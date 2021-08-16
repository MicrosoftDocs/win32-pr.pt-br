---
title: Data e hora efetivas
description: A data e a hora efetivas são uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos das informações para algum ponto no futuro quando a alteração tem uma alta probabilidade de ser totalmente replicada.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d95c80627c878bbc9d8cb6ac16436e6dae3e12cf262e797724cd5053f371ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695359"
---
# <a name="effective-date-and-time"></a>Data e hora efetivas

A data *e* a hora efetivas são uma estratégia de prevenção que impede a distorção de versão e atualizações parciais, adiando os dados efetivos das informações para algum ponto no futuro quando a alteração tem uma alta probabilidade de ser totalmente replicada. Para implementar datas efetivas, os objetos de aplicativo devem incluir um data/hora efetivo, que é preenchido quando o objeto é criado ou alterado. Os consumidores dos objetos verificam o timestamp e adiam o uso dos objetos até que a data e a hora sejam atingidas.

Algumas considerações importantes:

-   Os aplicativos que escolhem essa abordagem devem garantir que haja um conjunto de dados aplicáveis a ser usado até que os objetos atualizados se tornem efetivos.
-   O serviço de horário distribuído Windows NT 4.0 mantém os relógios do Windows 2000 sincronizados. No entanto, nenhum serviço de horário é perfeito, portanto, há uma pequena janela para distorção de versão.
-   Definir uma boa data efetiva presume o conhecimento da latência geral de replicação para o sistema distribuído em questão. Em uma rede estável, uma boa regra geral para datas efetivas é a (hora da atualização) + (2 \* (latência geral média)). Portanto, para um sistema cuja latência geral média de 4 horas, um atraso de 8 horas é razoável.
-   Em uma rede instável, determinar um valor "bom" para datas efetivas é muito mais difícil, pois a latência pode ser altamente variável. A data efetiva é mais "efetiva" em uma rede instável quando combinada com outras estratégias de prevenção ou detecção, como somas de verificação ou GUIDs de consistência. Para obter mais informações, consulte [Somas de verificação e contagens de objetos](checksums-and-object-counts.md).

 

 




