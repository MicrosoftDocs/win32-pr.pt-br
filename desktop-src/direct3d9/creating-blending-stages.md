---
description: Um estágio de mesclagem é um conjunto de operações de textura e seus argumentos que definem como as texturas são combinadas.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Criando estágios de mesclagem (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089237"
---
# <a name="creating-blending-stages-direct3d-9"></a>Criando estágios de mesclagem (Direct3D 9)

Um estágio de mesclagem é um conjunto de operações de textura e seus argumentos que definem como as texturas são combinadas. Ao fazer um estágio de mesclagem, os aplicativos C++ invocam o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . A primeira chamada especifica a operação que é executada. Duas invocações adicionais definem os argumentos aos quais a operação é aplicada. O exemplo de código a seguir ilustra a criação de um estágio de mesclagem.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



Os dados de Texel em texturas contêm valores de cor e alfa. Os aplicativos podem definir operações separadas para valores de cor e alfa em um único estágio de mesclagem. Cada operação, cor e alfa têm seus próprios argumentos. Para obter detalhes, consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Embora não faça parte da API do Direct3D, você pode inserir as macros a seguir em seu aplicativo para abreviar o código necessário para criar estágios de mesclagem de textura.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> </dl>

 

 
