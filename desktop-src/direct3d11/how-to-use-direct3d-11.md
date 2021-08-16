---
title: Como usar o Direct3D 11
description: Esta seção demonstra como usar a API do Microsoft Direct3D 11 para realizar várias tarefas comuns.
ms.assetid: 9BDEDB68-3484-4683-85AF-B583971382C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5613a2ea9a4b8c472c7483e9e29d5ce2d5d2ffccbd3b4ee7d8c65a1621e88c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633046"
---
# <a name="how-to-use-direct3d-11"></a>Como usar o Direct3D 11

Esta seção demonstra como usar a API do Microsoft Direct3D 11 para realizar várias tarefas comuns.



| Tópico                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como: criar um dispositivo de referência](overviews-direct3d-11-devices-create-ref.md)<br/>                                  | Este tópico mostra como criar um dispositivo de referência que implementa uma implementação de software altamente precisa do tempo de execução.<br/>                                                                                                                                                    |
| [Como: criar um dispositivo de detorção](overviews-direct3d-11-devices-create-warp.md)<br/>                                      | Este tópico mostra como criar um dispositivo de detorção que implementa um rasterizador de software de alta velocidade.<br/>                                                                                                                                                                                  |
| [Como: criar uma cadeia de permuta](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                 | Este tópico mostra como criar uma cadeia de permuta que encapsula dois ou mais buffers que são usados para renderização e exibição. <br/>                                                                                                                                                      |
| [Como enumerar adaptadores](overviews-direct3d-11-devices-enum.md)<br/>                                               | Este tópico mostra como usar o DXGI (infra-estrutura de gráficos do Microsoft DirectX) para enumerar os adaptadores gráficos disponíveis em um computador.<br/>                                                                                                                                        |
| [Como: obter modos de exibição do adaptador](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                            | Este tópico mostra como usar DXGI para obter os modos de exibição válidos associados a um adaptador.<br/>                                                                                                                                                                                     |
| [Como: criar um dispositivo e um contexto imediato](overviews-direct3d-11-devices-initialize.md)<br/>                      | Este tópico mostra como inicializar um [dispositivo](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                                                                                                        |
| [Como: obter o nível de recurso do dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/>                            | Este tópico mostra como obter o nível de [recurso](overviews-direct3d-11-devices-downlevel-intro.md) mais alto com suporte de um [dispositivo](overviews-direct3d-11-devices-intro.md).<br/>                                                                                                   |
| [Como criar um buffer de vértice](overviews-direct3d-11-resources-buffers-vertex-how-to.md)<br/>                        | Este tópico mostra como inicializar um buffer de [vértices](overviews-direct3d-11-resources-buffers-intro.md)estáticos, ou seja, um buffer de vértice que não é alterado.<br/>                                                                                                                  |
| [Como: criar um buffer de índice](overviews-direct3d-11-resources-buffers-index-how-to.md)<br/>                         | Este tópico mostra como inicializar um [buffer de índice](overviews-direct3d-11-resources-buffers-intro.md) em preparação para renderização.<br/>                                                                                                                                           |
| [Como: criar um buffer de constantes](overviews-direct3d-11-resources-buffers-constant-how-to.md)<br/>                    | Este tópico mostra como inicializar um [buffer de constantes](overviews-direct3d-11-resources-buffers-intro.md) na preparação para renderização.<br/>                                                                                                                                         |
| [Como: criar uma textura](overviews-direct3d-11-resources-textures-create.md)<br/>                                    | Este tópico mostra como criar uma textura.<br/>                                                                                                                                                                                                                                       |
| [Como: inicializar uma textura programaticamente](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)<br/> | Este tópico tem vários exemplos que mostram como inicializar texturas criadas com diferentes tipos de usos.<br/>                                                                                                                                                             |
| [Como: inicializar uma textura a partir de um arquivo](overviews-direct3d-11-resources-textures-how-to.md)<br/>                    | este tópico mostra como usar o componente de Windows Imaging (WIC) para criar a textura e a exibição separadamente.<br/>                                                                                                                                                                      |
| [Como: usar recursos dinâmicos](how-to--use-dynamic-resources.md)<br/>                                                 | Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar os dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.<br/>                                                                                                                              |
| [Como: criar um sombreador de computação](direct3d-11-advanced-stages-compute-create.md)<br/>                                  | Este tópico mostra como criar um sombreador de computação.<br/>                                                                                                                                                                                                                                |
| [Como criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                 | Este tópico mostra como criar um sombreador envoltória.<br/>                                                                                                                                                                                                                                  |
| [Como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                 | Este tópico mostra como criar um sombreador envoltória.<br/>                                                                                                                                                                                                                                   |
| [Como inicializar o estágio Tessellator](direct3d-11-advanced-stages-tessellator-initialize.md)<br/>                 | Este tópico mostra como inicializar o estágio Tessellator.<br/>                                                                                                                                                                                                                       |
| [Como criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                             | Este tópico mostra como criar um sombreador de domínio.<br/>                                                                                                                                                                                                                                |
| [Como: criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                             | Este tópico mostra como criar um sombreador de domínio.<br/>                                                                                                                                                                                                                                 |
| [Como: compilar um sombreador](how-to--compile-a-shader.md)<br/>                                                           | Este tópico mostra como usar a função [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) em tempo de execução para compilar o código de sombreador.<br/>                                                                                                                                          |
| [Como gravar uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-record.md)<br/>                 | Este tópico mostra como criar e registrar uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                         |
| [Como reproduzir uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md)<br/>                | Este tópico mostra como reproduzir uma lista de [comandos](overviews-direct3d-11-render-multi-thread-command-list.md).<br/>                                                                                                                                                                 |
| [Como: verificar o suporte de driver](overviews-direct3d-11-render-multi-thread-support.md)<br/>                          | Este tópico mostra como determinar se os recursos de multithreading (incluindo a [criação de recursos](overviews-direct3d-11-render-multi-thread-intro.md) e as [listas de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)) têm suporte para aceleração de hardware.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos gráficos do Direct3D 11](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

