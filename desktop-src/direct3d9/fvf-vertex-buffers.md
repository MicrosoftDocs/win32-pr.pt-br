---
description: 'Definir o parâmetro FVF do método IDirect3DDevice9:: CreateVertexBuffer como um valor diferente de zero, que deve ser um código FVF válido, indica que o conteúdo do buffer será caracterizado por um código FVF.'
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Buffers de vértice FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786318"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Buffers de vértice FVF (Direct3D 9)

Definir o parâmetro FVF do método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) como um valor diferente de zero, que deve ser um código FVF válido, indica que o conteúdo do buffer será caracterizado por um código FVF. Um buffer de vértice que é criado com um código FVF é chamado de buffer de vértice FVF. Alguns métodos ou usos de [**IDirect3DDevice9**](/windows/desktop/api) exigem buffers de vértices FVF e outros exigem buffers de vértices não FVF. Os buffers de vértice FVF são necessários como o argumento de buffer de vértice de destino para [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).

Os buffers de vértice FVF podem ser associados a um fluxo de dados de origem para qualquer número de fluxo.

A presença do componente D3DFVF \_ XYZRHW em buffers de vértices FVF indica que os vértices nesse buffer foram processados. Buffers de vértices usados para [**IDirect3DDevice9:P:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) os buffers de vértice de destino rocessvertices devem ser pós-processamento. Os buffers de vértice usados para entradas de sombreador de função fixa podem ser pré-processados ou pré-processados. Se o buffer de vértice for pós-processamento, o sombreador será efetivamente ignorado e os dados serão passados diretamente para o módulo de recorte e configuração primitivos.

Os buffers de vértice FVF podem ser usados com sombreadores de vértice. Além disso, os fluxos de vértice podem representar os mesmos formatos de vértice que os buffers de vértice não FVF. Eles não precisam ser usados para inserir dados de buffers de vértices separados. A flexibilidade adicional dos novos fluxos de vértice permite que os aplicativos que precisam manter seus dados separados funcionem melhor, mas não são necessários. Se o aplicativo puder manter dados intercalados antecipadamente, isso será um aumento de desempenho. Se o aplicativo apenas intercalar os dados antes de cada chamada de renderização, ele deve habilitar a API ou o hardware para fazer isso com vários fluxos.

As coisas mais importantes com o desempenho do vértice é usar um vértice de 32 bytes e manter uma boa ordem de cache.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
