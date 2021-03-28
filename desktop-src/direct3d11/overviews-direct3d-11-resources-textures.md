---
title: Texturas
description: Esta seção descreve as texturas usadas no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160129"
---
# <a name="textures"></a>Texturas

Uma textura armazena informações de Texel. Esta seção descreve as texturas usadas no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução às texturas no Direct3D 11](overviews-direct3d-11-resources-textures-intro.md)<br/> | Um recurso de textura é uma coleção estruturada de dados projetada para armazenar texels. Um texel representa a menor unidade de uma textura que pode ser lida ou gravada pelo pipeline. Diferente dos buffers, as texturas podem ser filtradas por amostras de texturas à medida que são lidas por unidades de sombreador. O tipo de textura afeta como a textura é filtrada. Cada Texel contém de 1 a 4 componentes, organizados em um dos formatos DXGI definidos pela enumeração de \_ formato dxgi.<br/> |
| [Compactação de bloco de textura no Direct3D 11](texture-block-compression-in-direct3d-11.md)<br/>      | O suporte para texturas de compactação de bloco (BC) foi estendido no Direct3D 11 para incluir os algoritmos de BC6H e BC7. O BC6H dá suporte a dados de origem de cor de intervalo altamente dinâmico e o BC7 fornece compactação de qualidade melhor que a média com menos artefatos para dados de origem RGB padrão.<br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como: criar uma textura](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[Como: inicializar uma textura programaticamente](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[Como: inicializar uma textura a partir de um arquivo](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





