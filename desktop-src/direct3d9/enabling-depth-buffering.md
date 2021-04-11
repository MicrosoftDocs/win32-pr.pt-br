---
description: 'Depois de criar um buffer de profundidade, conforme descrito em criando um buffer de profundidade (Direct3D 9), habilite o buffer de profundidade chamando o método IDirect3DDevice9:: setrenderingstate.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Habilitando o buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295934"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Habilitando o buffer de profundidade (Direct3D 9)

Depois de criar um buffer de profundidade, conforme descrito em [criando um buffer de profundidade (Direct3D 9)](creating-a-depth-buffer.md), habilite o buffer de profundidade chamando o método [**IDirect3DDevice9:: setrenderingstate**](/windows/desktop/api) . Defina o \_ estado de RENDERIZAÇÃO D3DRS ZENABLE para habilitar o buffer de profundidade. Use o \_ membro true do D3DZB do tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (ou **true**) para habilitar o z-buffer, D3DZB \_ USEW para habilitar o w-buffer ou D3DZB \_ false (ou **false**) para desabilitar o buffer de profundidade.

> [!Note]  
> Para usar o w-Buffering, seu aplicativo deve definir uma matriz de projeção compatível mesmo que ela não use o pipeline de transformação do Direct3D. Para obter informações sobre como fornecer uma matriz de projeção apropriada, consulte [uma matriz de projeção amigável W](projection-transform.md)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
