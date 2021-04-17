---
title: Tabelas de funções virtuais
description: Tabelas de funções virtuais
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105751415"
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



 

 




