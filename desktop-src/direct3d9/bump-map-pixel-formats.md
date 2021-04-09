---
description: Um mapa de relevo é um objeto IDirect3DTexture9 que usa um formato de pixel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de pixel do mapa de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010257"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formatos de pixel do mapa de relevo (Direct3D 9)

Um mapa de relevo é um objeto [**IDirect3DTexture9**](/windows/desktop/api) que usa um formato de pixel especializado. Em vez de armazenar componentes de cores vermelho, verde e azul, cada pixel em um mapa de relevo armazena os valores Delta para você e v (D<sub>U</sub> e d<sub>v</sub>) e, às vezes, um componente de luminância, L. Esses valores são aplicados pelo sistema, conforme descrito no tópico [fórmulas de mapeamento de relevo (Direct3D 9)](bump-mapping-formulas.md) .

Você pode especificar um formato de pixel do mapa de relevo definindo o formato como um dos seguintes: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 ou D3DFMT \_ V16U16. Para obter descrições, consulte [D3DFORMAT](d3dformat.md).

Os componentes D<sub>U</sub> e d<sub>V</sub> de um pixel são valores assinados que variam de-1,0 a + 1,0. O componente de luminância, quando usado, é um valor inteiro sem sinal que varia de 0 a 255.

> [!Note]  
> Antes de escolher um formato de pixel do mapa de relevo, verifique se há suporte para o formato específico. Para obter mais informações, consulte [usando o mapeamento de relevo (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de relevo](bump-mapping.md)
</dt> </dl>

 

 



