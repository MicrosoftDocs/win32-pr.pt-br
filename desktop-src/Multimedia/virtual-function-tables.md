---
title: Tabelas de funções virtuais
description: Tabelas de funções virtuais
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135493"
---
# <a name="virtual-function-tables"></a>Tabelas de funções virtuais

Uma tabela de funções virtuais é uma matriz de ponteiros para os métodos aos quais um objeto dá suporte. Se você estiver usando C, um objeto aparecerá como uma estrutura cujo primeiro membro é um ponteiro para a tabela de funções virtuais (**lpVtbl**); ou seja, o primeiro membro aponta para uma matriz que contém ponteiros de função. Todos os métodos assumem um ponteiro para a tabela de funções como o primeiro parâmetro. Assim, o exemplo a seguir chama o método **Read** de um objeto **pStream** :


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



Em C + +, o ponteiro para a *tabela de funções virtuais, o ponteiro* , é implícito. O seguinte é equivalente ao exemplo anterior ao usar o C + +:


```C++
pStream->Read(parameters) 
 
```



 

 




