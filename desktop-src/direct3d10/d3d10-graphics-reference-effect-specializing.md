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
# <a name="specializing-interfaces-direct3d-10"></a>Interfaces especializadas (Direct3D 10)

A [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) tem vários métodos para converter a interface no tipo específico de interface de que você precisa. Os métodos estão no formato como *tipo* e incluem um método para cada tipo de variável de efeito (como asblend, AsConstantBuffer, etc.)

Por exemplo, suponha que você tenha um efeito com duas variáveis globais: hora e uma transformação do mundo.


```
float    g_fTime;
float4x4 g_mWorld;
```



Aqui está um exemplo (de [exemplo de SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) que obtém estas variáveis:


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Ao especializar as interfaces, você pode reduzir o código para uma única chamada.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



As interfaces que herdam da [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) também têm esses métodos, mas foram projetadas para retornar objetos inválidos; Somente chamadas da **interface ID3D10EffectVariable** retornam objetos válidos. Os aplicativos podem testar o objeto retornado para ver se ele é válido chamando [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Effect](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



