---
title: Restrições de uso de interface
description: O hardware de GPU atual não dá suporte a informações de slot variáveis no tempo de execução do sombreador. Como consequência, as referências de interface não podem ser modificadas em uma expressão condicional, como uma instrução If ou switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292030"
---
# <a name="interface-usage-restrictions"></a><span data-ttu-id="00282-104">Restrições de uso de interface</span><span class="sxs-lookup"><span data-stu-id="00282-104">Interface Usage Restrictions</span></span>

<span data-ttu-id="00282-105">O hardware de GPU atual não dá suporte a informações de slot variáveis no tempo de execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="00282-105">Current GPU hardware does not support varying slot information at shader runtime.</span></span> <span data-ttu-id="00282-106">Como consequência, as referências de interface não podem ser modificadas em uma expressão condicional, como uma instrução If ou switch.</span><span class="sxs-lookup"><span data-stu-id="00282-106">As a consequence interface references cannot be modified within a conditional expression such as an if or switch statement.</span></span>

<span data-ttu-id="00282-107">O código do sombreador a seguir ilustra quando essa restrição ocorrerá e uma possível abordagem alternativa.</span><span class="sxs-lookup"><span data-stu-id="00282-107">The following shader code illustrates when this restriction will occur and a possible alternate approach.</span></span>

<span data-ttu-id="00282-108">Dadas as seguintes declarações de interface:</span><span class="sxs-lookup"><span data-stu-id="00282-108">Given the following interface declarations:</span></span>


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



<span data-ttu-id="00282-109">Dadas as seguintes declarações de classe:</span><span class="sxs-lookup"><span data-stu-id="00282-109">Given the following class declarations:</span></span>


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



<span data-ttu-id="00282-110">Uma referência de interface não pode ser modificada dentro da expressão condicional (uma instrução If):</span><span class="sxs-lookup"><span data-stu-id="00282-110">An interface reference cannot be modified within the conditional expression (an if statement):</span></span>


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



<span data-ttu-id="00282-111">Dada a mesma interface e declarações de classe, você pode usar um índice para fornecer a mesma funcionalidade e evitar o loop forçado de desroll.</span><span class="sxs-lookup"><span data-stu-id="00282-111">Given the same interface and class declarations, you could use an index to provide the same functionality and avoid the forced loop unroll.</span></span>


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a><span data-ttu-id="00282-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00282-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00282-113">Vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="00282-113">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




