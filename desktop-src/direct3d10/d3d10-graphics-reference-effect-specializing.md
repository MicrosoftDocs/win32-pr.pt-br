---
description: A interface ID3D10EffectVariable tem vários métodos para converter a interface no tipo específico de interface de que você precisa.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Interfaces especializadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750565"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="fdfaf-103">Interfaces especializadas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fdfaf-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="fdfaf-104">A [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) tem vários métodos para converter a interface no tipo específico de interface de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="fdfaf-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="fdfaf-105">Os métodos estão no formato como *tipo* e incluem um método para cada tipo de variável de efeito (como asblend, AsConstantBuffer, etc.)</span><span class="sxs-lookup"><span data-stu-id="fdfaf-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="fdfaf-106">Por exemplo, suponha que você tenha um efeito com duas variáveis globais: hora e uma transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="fdfaf-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="fdfaf-107">Aqui está um exemplo (de [exemplo de SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) que obtém estas variáveis:</span><span class="sxs-lookup"><span data-stu-id="fdfaf-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="fdfaf-108">Ao especializar as interfaces, você pode reduzir o código para uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="fdfaf-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="fdfaf-109">As interfaces que herdam da [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) também têm esses métodos, mas foram projetadas para retornar objetos inválidos; Somente chamadas da **interface ID3D10EffectVariable** retornam objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="fdfaf-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="fdfaf-110">Os aplicativos podem testar o objeto retornado para ver se ele é válido chamando [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span><span class="sxs-lookup"><span data-stu-id="fdfaf-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdfaf-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdfaf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdfaf-112">Effect</span><span class="sxs-lookup"><span data-stu-id="fdfaf-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



