---
title: Vários controles em uma DLL
description: Vários controles em uma DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004950"
---
# <a name="multiple-controls-in-one-dll"></a>Vários controles em uma DLL

Uma única DLL. ocx pode contêinerar qualquer número de controles ActiveX, simplificando assim a distribuição e o uso de um conjunto de controles relacionados.

Se você enviar vários controles em uma única DLL, certifique-se de incluir o nome do fornecedor em cada nome de controle no pacote. A inclusão dos nomes dos fornecedores em cada nome de controle permitirá que os usuários identifiquem facilmente os controles em um pacote. Por exemplo, se você enviar uma DLL que implemente três controles, Con1, Con2 e Con3, os nomes de controle deverão ser:

-   *O nome da sua empresa* Controle Con1

-   *O nome da sua empresa* Controle Con2

-   *O nome da sua empresa* Controle Con3

 

 




