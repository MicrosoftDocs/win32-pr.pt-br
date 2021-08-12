---
description: O Direct3D 9 dá suporte a texturas paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755abb638ab1dd94e25edd98b2daef5e65d5a54cca7baf21a74e7d06173eed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291161"
---
# <a name="texture-palettes-direct3d-9"></a>Paletas de textura (Direct3D 9)

O Direct3D 9 dá suporte a texturas paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Uma paleta se atualiza chamando o [**método IDirect3DDevice9::SetCurrentTexturePalette.**](/windows/desktop/api) A paleta atual é usada para traduzir todas as texturas paletas para todos os estágios de textura ativos. [**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) atualiza todas as 256 entradas de uma paleta. Cada entrada é uma [**estrutura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) do formato D3DFMT \_ A8R8G8B8. Todas as entradas são padrão 0xFFFFFFFF.

As [**paletas IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contêm um canal alfa. Esse canal alfa pode ser usado quando o sinalizador de funcionalidade do dispositivo ALPHAPALETTE D3DPTEXTURECAPS está definido, indicando que o dispositivo dá suporte a alfa da \_ paleta. O canal alfa da paleta é usado quando o formato de textura não tem um canal alfa. Se o dispositivo não dá suporte a alfa da paleta e o formato de textura não tem um canal alfa, um valor de 0xFF é usado para alfa.

Há um máximo de 65.536 (0x0000FFFF) paletas. Como os recursos de memória associados ao conjunto de paletas são proporcionais ao número máximo de paletas referenciados por um aplicativo, use números de paleta contígua começando em zero.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
