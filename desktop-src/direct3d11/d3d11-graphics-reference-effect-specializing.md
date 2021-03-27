---
title: Interfaces especializadas (Direct3D 11)
description: O ID3DX11EffectVariable tem vários métodos para converter a interface no tipo específico de interface de que você precisa.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636425"
---
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="c7612-103">Interfaces especializadas (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c7612-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="c7612-104">O [**ID3DX11EffectVariable**](id3dx11effectvariable.md) tem vários métodos para converter a interface no tipo específico de interface de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="c7612-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="c7612-105">Os métodos estão no formato *tipo* e incluem um método para cada tipo de variável de efeito (como asblend, AsConstantBuffer, etc.).</span><span class="sxs-lookup"><span data-stu-id="c7612-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="c7612-106">Por exemplo, suponha que você tenha um efeito com duas variáveis globais: hora e uma transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="c7612-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="c7612-107">Aqui está um exemplo que obtém essas variáveis:</span><span class="sxs-lookup"><span data-stu-id="c7612-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="c7612-108">Ao especializar as interfaces, você pode reduzir o código para uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="c7612-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="c7612-109">As interfaces que herdam de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) também têm esses métodos, mas foram projetadas para retornar objetos inválidos; Somente chamadas de **ID3DX11EffectVariable** retornam objetos válidos.</span><span class="sxs-lookup"><span data-stu-id="c7612-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="c7612-110">Os aplicativos podem testar o objeto retornado para ver se ele é válido chamando [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="c7612-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7612-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7612-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7612-112">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c7612-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




