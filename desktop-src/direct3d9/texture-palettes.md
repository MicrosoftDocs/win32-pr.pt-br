---
description: O Direct3D 9 dá suporte a texturas de paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796228"
---
# <a name="texture-palettes-direct3d-9"></a>Paletas de textura (Direct3D 9)

O Direct3D 9 dá suporte a texturas de paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Uma paleta é tornada atual chamando o método [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) . A paleta atual é usada para traduzir todas as texturas da paleta para todos os estágios de textura ativas. [**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) atualiza todas as entradas 256 de uma paleta. Cada entrada é uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) do formato D3DFMT \_ A8R8G8B8. Todas as entradas assumem o padrão de 0xFFFFFFFF.

As paletas [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contêm um canal alfa. Esse canal alfa pode ser usado quando o \_ sinalizador de recurso de dispositivo D3DPTEXTURECAPS ALPHAPALETTE é definido, indicando que o dispositivo dá suporte a alfa da paleta. O canal alfa da paleta é usado quando o formato de textura não tem um canal alfa. Se o dispositivo não oferecer suporte a alfa da paleta e o formato de textura não tiver um canal alfa, um valor de 0xFF será usado para alfa.

Há um máximo de 65.536 de paletas (0x0000FFFF). Como os recursos de memória associados ao conjunto de paletas são proporcionais ao número máximo de paleta que um aplicativo faz referência, use números de paleta contíguos começando em zero.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
