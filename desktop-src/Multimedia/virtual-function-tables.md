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
# <a name="virtual-function-tables"></a><span data-ttu-id="f2a16-103">Tabelas de funções virtuais</span><span class="sxs-lookup"><span data-stu-id="f2a16-103">Virtual Function Tables</span></span>

<span data-ttu-id="f2a16-104">Uma tabela de funções virtuais é uma matriz de ponteiros para os métodos aos quais um objeto dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f2a16-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="f2a16-105">Se você estiver usando C, um objeto aparecerá como uma estrutura cujo primeiro membro é um ponteiro para a tabela de funções virtuais (**lpVtbl**); ou seja, o primeiro membro aponta para uma matriz que contém ponteiros de função.</span><span class="sxs-lookup"><span data-stu-id="f2a16-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="f2a16-106">Todos os métodos assumem um ponteiro para a tabela de funções como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f2a16-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="f2a16-107">Assim, o exemplo a seguir chama o método **Read** de um objeto **pStream** :</span><span class="sxs-lookup"><span data-stu-id="f2a16-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="f2a16-108">Em C + +, o ponteiro para a *tabela de funções virtuais, o ponteiro* , é implícito.</span><span class="sxs-lookup"><span data-stu-id="f2a16-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="f2a16-109">O seguinte é equivalente ao exemplo anterior ao usar o C + +:</span><span class="sxs-lookup"><span data-stu-id="f2a16-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 




