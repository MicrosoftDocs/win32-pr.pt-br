---
title: Multithreading
description: O Direct3D 11 implementa suporte para criação e renderização de objetos usando vários threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718d80d9b70db0d6102d746168f338ddd8099339cee349724d87036714b16580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124321"
---
# <a name="multithreading"></a>Multithreading

O Direct3D 11 implementa suporte para criação e renderização de objetos usando vários threads.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                   | Descrição                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução a multithreading no Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Multithreading foi projetado para melhorar o desempenho executando o trabalho usando um ou mais threads ao mesmo tempo. <br/>                                                                                                         |
| [Criação de objeto com multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Use a interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para criar recursos e objetos, use [**o ID3D11DeviceContext para**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) [renderizar](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | O Direct3D 11 dá suporte a dois tipos de renderização: imediato e adiado. Ambos são implementados usando a interface [**ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/>                                                      |
| [Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Uma lista de comandos é uma sequência de comandos gpu que podem ser gravados e gravados. Uma lista de comandos pode melhorar o desempenho reduzindo a quantidade de sobrecarga gerada pelo runtime.<br/>                                    |
| [Diferenças de threading entre versões do Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Muitos modelos de programação multi-threaded usam primitivos de sincronização (como mutexes) para criar seções críticas e impedir que o código seja acessado por mais de um thread por vez.<br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como verificar se há suporte para driver](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Renderização](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





