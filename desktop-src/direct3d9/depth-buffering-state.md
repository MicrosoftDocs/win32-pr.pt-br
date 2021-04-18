---
description: O buffer de profundidade é um método de remoção de linhas ocultas e superfícies. Por padrão, o Direct3D não usa o buffer de profundidade.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Estado de buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456583"
---
# <a name="depth-buffering-state-direct3d-9"></a>Estado de buffer de profundidade (Direct3D 9)

O buffer de profundidade é um método de remoção de linhas ocultas e superfícies. Por padrão, o Direct3D não usa o buffer de profundidade.

Para obter uma visão geral conceitual dos buffers de profundidade, consulte [buffers de profundidade (Direct3D 9)](depth-buffers.md).

Os aplicativos C++ atualizam o estado de buffer de profundidade com o \_ estado de RENDERIZAÇÃO D3DRS ZENABLE, usando um membro da enumeração [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) para especificar o novo valor de estado.

Se seu aplicativo precisar impedir que o Direct3D grave no buffer de profundidade, ele poderá usar o \_ valor enumerado D3DRS ZWRITEENABLE, ESPECIFICANDO D3DZB \_ false como o segundo parâmetro para a chamada para [**IDirect3DDevice9:: setprocessstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

O exemplo de código a seguir mostra como o estado do buffer de profundidade é definido para habilitar o z-buffer.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



Seu aplicativo também pode usar o \_ estado de RENDERIZAÇÃO D3DRS ZFUNC para controlar a função de comparação que o Direct3D usa ao executar o buffer de profundidade.

A tendência Z é um método de exibir uma superfície na frente de outra, mesmo que seus valores de profundidade sejam os mesmos. Você pode usar essa técnica para uma variedade de efeitos. Um exemplo comum é A renderização de sombras em paredes. Tanto a sombra quanto a parede têm o mesmo valor de profundidade. No entanto, você deseja que seu aplicativo mostre a sombra na parede. Dar uma tendência z à sombra faz com que o Direct3D as exiba corretamente (Confira D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
