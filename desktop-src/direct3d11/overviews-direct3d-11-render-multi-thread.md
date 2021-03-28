---
title: MultiThreading
description: O Direct3D 11 implementa o suporte para a criação e renderização de objetos usando vários threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160132"
---
# <a name="multithreading"></a>MultiThreading

O Direct3D 11 implementa o suporte para a criação e renderização de objetos usando vários threads.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                   | Descrição                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução a multithreading no Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | O multithreading foi projetado para melhorar o desempenho executando o trabalho usando um ou mais threads ao mesmo tempo. <br/>                                                                                                         |
| [Criação de objeto com multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Use a interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para criar recursos e objetos, use o [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para [renderização](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | O Direct3D 11 dá suporte a dois tipos de renderização: Immediate e adiada. Ambos são implementados usando a interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .<br/>                                                      |
| [Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Uma lista de comandos é uma sequência de comandos de GPU que podem ser gravados e reproduzidos. Uma lista de comandos pode melhorar o desempenho, reduzindo a quantidade de sobrecarga gerada pelo tempo de execução.<br/>                                    |
| [Diferenças de Threading entre versões do Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Muitos modelos de programação multi-threaded usam primitivos de sincronização (como mutexes) para criar seções críticas e impedir que o código seja acessado por mais de um thread por vez.<br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como: verificar o suporte de driver](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Renderização](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





