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
# <a name="specializing-interfaces-direct3d-11"></a>Interfaces especializadas (Direct3D 11)

O [**ID3DX11EffectVariable**](id3dx11effectvariable.md) tem vários métodos para converter a interface no tipo específico de interface de que você precisa. Os métodos estão no formato *tipo* e incluem um método para cada tipo de variável de efeito (como asblend, AsConstantBuffer, etc.).

Por exemplo, suponha que você tenha um efeito com duas variáveis globais: hora e uma transformação do mundo.


```
float    g_fTime;
float4x4 g_mWorld;
```



Aqui está um exemplo que obtém essas variáveis:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Ao especializar as interfaces, você pode reduzir o código para uma única chamada.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



As interfaces que herdam de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) também têm esses métodos, mas foram projetadas para retornar objetos inválidos; Somente chamadas de **ID3DX11EffectVariable** retornam objetos válidos. Os aplicativos podem testar o objeto retornado para ver se ele é válido chamando [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




