---
description: O termo blit é a abreviação de &\# 0034; transferência de bloco de bits, &\# 0034; que é o processo de transferência de blocos de dados de um local na memória para outro.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copiando superfícies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796117"
---
# <a name="copying-surfaces-direct3d-9"></a>Copiando superfícies (Direct3D 9)

O termo blit é a abreviação de "transferência de bloco de bits", que é o processo de transferência de blocos de dados de um local na memória para outro. A interface de driver de dispositivo de transferência de bits (DDI) continua sendo usada no Direct3D 9 como o mecanismo principal para mover grandes retângulos de pixels em uma base por quadro, o mecanismo por trás do IDirect3DDevice9 orientado a cópia [**::P método reenviado**](/windows/desktop/api) . O transporte do trabalho artístico na operação blit é executado pelo método [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) . O trabalho artístico também pode ser copiado no Direct3D 9 usando o método [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , que copia um subconjunto retangular de pixels.

> [!Note]  
> O Direct3D 9 fornece funções D3DX que permitem que você carregue a arte de arquivos, aplique a conversão de cores e redimensione a arte. Para obter mais informações sobre as funções disponíveis, consulte [funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
