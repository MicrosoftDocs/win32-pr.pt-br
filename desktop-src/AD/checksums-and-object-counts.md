---
title: Somas de verificação e contagens de objetos
description: Somas de verificação e contagens de objetos são estratégias de detecção que permitem que um aplicativo detecte um estado de atualização parcial.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453474"
---
# <a name="checksums-and-object-counts"></a>Somas de verificação e contagens de objetos

Somas de verificação e contagens de objetos são estratégias de detecção que permitem que um aplicativo detecte um estado de atualização parcial. As somas de verificação também podem ser usadas para detectar inconsistências introduzidas pela resolução de colisão. As somas de verificação e as contagens de objeto exigem um local para armazenar o valor usado para verificar uma soma de verificação ou contagem de objetos. Isso pode ser um objeto "mestre" escolhido entre os envolvidos na relação específica do aplicativo ou em um objeto pai sob o qual os objetos relacionados são armazenados.

Para somas de verificação, os aplicativos que lêem os objetos relacionados verificam a soma de verificação calculando um resultado local e comparando-o com o valor armazenado. Se os valores não corresponderem, a réplica estará em um estado de atualização parcial e os objetos não poderão ser usados.

Para contagens de objetos, os aplicativos contam os objetos relacionados (normalmente filhos de um único pai) e comparam a contagem com o valor armazenado. Se as contagens não corresponderem, a réplica estará em um estado de atualização parcial e os objetos não poderão ser usados.

Algumas considerações importantes:

-   Para que a abordagem de soma de verificação funcione, é necessário atualizar um ou mais atributos usados na computação da soma de verificação. O algoritmo usado para calcular a soma de verificação deve refletir as diferenças na entrada de forma confiável. Se muitas entradas diferentes contiverem a mesma soma de verificação, o algoritmo não detectará as atualizações parciais de forma confiável. "Salting" a entrada com valores como o **objectGUID** do computador de origem e a data e hora da atualização também é útil.
-   As contagens de objetos funcionam melhor quando usadas com novos conjuntos de objetos ou em combinação com GUIDs de consistência (consulte a próxima seção para obter mais informações). O aplicativo que está executando a atualização deve saber, antecipadamente, o número de objetos que estarão no contêiner quando a atualização for concluída ou use outros meios de marcar o contêiner como inválido enquanto a atualização continuar (por exemplo, definindo a contagem como zero). Depois de concluir a atualização, o aplicativo de origem marca o contêiner com a contagem de objetos contidos.

 

 




