---
title: Interfaces especializadas (Direct3D 11)
description: O ID3DX11EffectVariable tem vários métodos para converter a interface no tipo específico de interface de que você precisa.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126070"
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

 

 




