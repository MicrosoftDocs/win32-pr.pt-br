---
title: O operador de resolução de escopo em C++
description: O operador de resolução de escopo em C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822661"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="7b29f-103">O operador de resolução de escopo em C++</span><span class="sxs-lookup"><span data-stu-id="7b29f-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="7b29f-104">Dois pontos-e-vírgulas (::) são usados em C++ como um operador de *resolução de escopo* .</span><span class="sxs-lookup"><span data-stu-id="7b29f-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="7b29f-105">Esse operador dá a você mais liberdade ao nomear suas variáveis, permitindo que você diferencie as variáveis com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="7b29f-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="7b29f-106">Por exemplo, *MyFile:: Read* refere-se ao método *Read* da classe *MyFile* de objetos, em oposição ao *seufile:: Read*, que se refere a um método *Read* na *sua* classe.</span><span class="sxs-lookup"><span data-stu-id="7b29f-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




