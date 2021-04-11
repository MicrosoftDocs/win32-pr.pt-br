---
title: Descarregamento de IAgent
description: Descarregamento de IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294031"
---
# <a name="iagentunload"></a><span data-ttu-id="0319d-103">IAgent:: UnLoad</span><span class="sxs-lookup"><span data-stu-id="0319d-103">IAgent::UnLoad</span></span>

<span data-ttu-id="0319d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0319d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="0319d-105">Descarrega os dados de caractere do caractere especificado da coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="0319d-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="0319d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0319d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0319d-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="0319d-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="0319d-108">A ID do caractere.</span><span class="sxs-lookup"><span data-stu-id="0319d-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="0319d-109">Use esse método quando não precisar mais de um caractere, para liberar memória usada para armazenar informações sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="0319d-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="0319d-110">Se você acessar o caractere novamente, use o método [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="0319d-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="0319d-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0319d-111">See Also</span></span>

[<span data-ttu-id="0319d-112">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="0319d-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 