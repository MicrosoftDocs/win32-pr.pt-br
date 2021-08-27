---
description: Um mapa de elevações é um objeto IDirect3DTexture9 que usa um formato de pixel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de pixel do mapa de elevações (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f627ce95151207c25e2365d2e467fb94b93cfb5c1bf54ce0c3df401891fcafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805721"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formatos de pixel do mapa de elevações (Direct3D 9)

Um mapa de elevações [**é um objeto IDirect3DTexture9**](/windows/desktop/api) que usa um formato de pixel especializado. Em vez de armazenar componentes de cor vermelho, verde e azul, cada pixel em um mapa de aumento armazena os valores delta para você e v (D<sub>U</sub> e D<sub>V</sub>) e, às vezes, um componente de luminância, L. Esses valores são aplicados pelo sistema, conforme descrito no tópico Fórmulas de mapeamento de aumento [(Direct3D 9).](bump-mapping-formulas.md)

Você pode especificar um formato de pixel do mapa de elevação definindo o formato como um dos seguintes: D3DFMT \_ CxV8U8, \_ D3DFMT V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 ou D3DFMT \_ V16U16. Para descrições, consulte [D3DFORMAT](d3dformat.md).

Os componentes<sub>D U</sub> e D<sub>V</sub> de um pixel são valores assinados que variam de - 1,0 a +1.0. O componente de luminância, quando usado, é um valor inteiro sem sinal que varia de 0 a 255.

> [!Note]  
> Antes de escolher um formato de pixel do mapa de elevações, verifique se há suporte para o formato específico. Para obter mais informações, consulte [Usando mapeamento de aumento (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de aumento](bump-mapping.md)
</dt> </dl>

 

 



