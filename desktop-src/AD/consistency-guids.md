---
title: GUIDs de consistência
description: Os GUIDs de consistência são uma estratégia de detecção que permite que um aplicativo detecte atualizações parciais.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004812"
---
# <a name="consistency-guids"></a>GUIDs de consistência

Os GUIDs de consistência são uma estratégia de detecção que permite que um aplicativo detecte atualizações parciais. Um GUID de consistência (identificador global exclusivo) é aplicado a cada objeto em um conjunto relacionado. Na implementação, um aplicativo de origem gera um novo GUID e o aplica a cada objeto que ele atualiza no conjunto de objetos relacionados. Em seguida, ele aplica o novo GUID ao restante dos objetos no conjunto e termina aplicando o novo GUID ao objeto "Master". Normalmente, o objeto "Master" será um contêiner que é o pai dos outros objetos no conjunto.

Algumas considerações importantes:

-   Os GUIDs de consistência combinados com contagens de objetos ou somas de verificação são mais eficazes do que os GUIDs de consistência sozinhos, pois o aplicativo que lê os objetos pode não saber quantos objetos com o GUID devem estar presentes.
-   Os aplicativos devem gerar seus próprios GUIDs (uma API do Microsoft Win32, UuidCreate, fornece essa função) e não usar os GUIDs gerados pelo sistema encontrados no atributo **objectGUID** de um objeto. Isso ocorre porque um GUID de consistência precisa ser alterado cada vez que o conjunto de objetos é atualizado. Os GUIDs de identidade do objeto encontrados no **objectGUID** nunca são alterados após a criação do objeto.
-   Os GUIDs de consistência pressupõem que nenhum objeto seja compartilhado entre os conjuntos, de modo que cada conjunto pode ter um GUID de consistência exclusivo.

 

 




