---
description: Um efeito é criado carregando-o na estrutura de efeitos.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Criar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760058"
---
# <a name="create-an-effect-direct3d-10"></a>Criar um efeito (Direct3D 10)

Um efeito é criado carregando-o na estrutura de efeitos. Se o efeito nunca tiver sido compilado, ele será compilado quando for criado. Os efeitos que já estão carregados na memória podem ser criados chamando [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). O exemplo de código a seguir usa [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) para criar um efeito de um arquivo.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



A leitura de um efeito requer os mesmos parâmetros que a compilação de um efeito, além de um dispositivo e um pool.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



