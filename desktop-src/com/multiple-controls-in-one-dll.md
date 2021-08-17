---
title: Vários controles em uma DLL
description: Vários controles em uma DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b571f307f3438ca8f8ce0a0a716af2042884520cd07746f8e6fa8c1739fae22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130058"
---
# <a name="multiple-controls-in-one-dll"></a>Vários controles em uma DLL

Uma única DLL .ocx pode colocar em contêiner qualquer número de controles ActiveX, simplificando assim a distribuição e o uso de um conjunto de controles relacionados.

Se você enviar vários controles em uma única DLL, inclua o nome do fornecedor em cada nome de controle no pacote. Incluir os nomes dos fornecedores em cada nome de controle permitirá que os usuários identifiquem facilmente os controles em um pacote. Por exemplo, se você enviar uma DLL que implementa três controles, Con1, Con2 e Con3, os nomes de controle deverão ser:

-   *Nome da sua empresa* Controle Con1

-   *Nome da sua empresa* Controle Con2

-   *Nome da sua empresa* Controle Con3

 

 




