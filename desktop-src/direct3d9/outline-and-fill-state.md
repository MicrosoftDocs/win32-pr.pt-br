---
description: Os primitivos que não têm texturas são renderizados com a cor especificada por seu material ou com as cores especificadas para os vértices, se houver.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Estrutura de tópicos e estado de preenchimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105790322"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Estrutura de tópicos e estado de preenchimento (Direct3D 9)

Os primitivos que não têm texturas são renderizados com a cor especificada por seu material ou com as cores especificadas para os vértices, se houver. Você pode selecionar o método para preenchê-los especificando um valor definido pelo tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) para o \_ estado de renderização FillMode D3DRS.

Para habilitar o pontilhamento, seu aplicativo deve passar o \_ valor enumerado D3DRS DITHERENABLE como o primeiro parâmetro para [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). Ele deve definir o segundo parâmetro como **true** para habilitar o pontilhamento e **false** para desabilitá-lo.

Às vezes, desenhar o último pixel em uma linha pode causar uma sobreposição insightável com primitivas ao redor. Você pode controlar isso usando o \_ valor enumerado D3DRS LASTPIXEL. No entanto, não altere essa configuração sem alguma reflexões. Em algumas condições, suprimir a renderização do último pixel pode causar falhas insightáveis entre primitivos.

Contornos de objeto podem ser desenhados definindo o padrão de desenho de linha apropriado. O estado de desenho de linha padrão é desenhar linhas sólidas. Para obter mais informações, consulte [suporte de desenho de linha no estado de RENDERIZAÇÃO D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
