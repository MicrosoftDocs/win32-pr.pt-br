---
description: O gerenciamento de recursos é o processo em que os recursos são promovidos do armazenamento de memória do sistema para o armazenamento acessível ao dispositivo e descartados do armazenamento acessível ao dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Gerenciando recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ef7a8be0e71c652b6e3f2ed467e866fd922791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163757"
---
# <a name="managing-resources-direct3d-9"></a>Gerenciando recursos (Direct3D 9)

O gerenciamento de recursos é o processo em que os recursos são promovidos do armazenamento de memória do sistema para o armazenamento acessível ao dispositivo e descartados do armazenamento acessível ao dispositivo. O tempo de execução do Direct3D tem seu próprio algoritmo de gerenciamento baseado em uma técnica de prioridade menos usada recentemente. O Direct3D alterna para uma técnica de prioridade usada mais recentemente quando detecta que mais recursos do que podem coexistir na memória acessível pelo dispositivo são usados em um único quadro-entre [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: endscenetion**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) calls.

Use o [**sinalizador \_ padrão D3DPOOL**](./d3dpool.md) no momento da criação para especificar que um recurso seja colocado no pool de memória mais apropriado para o conjunto de usos solicitados para o recurso fornecido. Normalmente, essa é a memória de vídeo, incluindo a memória local de vídeo e a memória AGP (Accelerated Graphics Port). Os recursos no pool padrão não persistem por meio de transições entre os Estados perdido e operacional do dispositivo. Esses recursos devem ser liberados antes de chamar Reset e, em seguida, devem ser recriados.

Use o [**sinalizador \_ gerenciado D3DPOOL**](./d3dpool.md) no momento da criação para especificar um recurso gerenciado. Os recursos gerenciados persistem por transições entre os Estados perdido e operacional do dispositivo. Esses recursos existem tanto na memória de vídeo quanto do sistema. Um recurso gerenciado será copiado para a memória de vídeo quando necessário durante a renderização. O dispositivo pode ser restaurado com uma chamada para [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), e esses recursos continuam funcionando normalmente sem serem recarregados com os dados. No entanto, se o dispositivo precisar ser destruído e recriado, todos os recursos deverão ser recriados.

O gerenciamento de recursos não é recomendado para recursos que mudam com alta frequência. Por exemplo, os buffers de vértice e de índice que são usados para atravessar um grafo de cena cada quadro que renderiza somente a geometria visível para o usuário altera todos os quadros. Como os recursos gerenciados são apoiados pela memória do sistema, as alterações constantes devem ser atualizadas na memória do sistema, o que pode causar uma degradação grave no desempenho. Para esse cenário específico, [**D3DPOOL \_ padrão**](./d3dpool.md) juntamente com [**D3DUSAGE \_ dinâmico**](d3dusage.md) deve ser usado.

Outro exemplo para o qual o gerenciamento de recursos não é recomendado (e explicitamente não permitido pelo tempo de execução) é o gerenciamento de uma textura criada com [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Se a memória usada pelos destinos de renderização fosse gerenciada pelo tempo de execução, o conteúdo teria de ser copiado constantemente para a memória do sistema durante o processamento, causando grandes penalidades de desempenho. Por esse motivo, os destinos de renderização devem ser criados no pool padrão. Se o acesso de CPU dos dados contidos em um destino de renderização for necessário, os dados deverão ser copiados para um recurso criado em [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usando [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api)ou [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Para obter mais informações sobre o estado perdido de um dispositivo, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
