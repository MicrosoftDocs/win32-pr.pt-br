---
description: O gerenciamento de recursos é o processo em que os recursos são promovidos do armazenamento de memória do sistema para o armazenamento acessível pelo dispositivo e descartados do armazenamento acessível pelo dispositivo.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Gerenciando recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728459"
---
# <a name="managing-resources-direct3d-9"></a>Gerenciando recursos (Direct3D 9)

O gerenciamento de recursos é o processo em que os recursos são promovidos do armazenamento de memória do sistema para o armazenamento acessível pelo dispositivo e descartados do armazenamento acessível pelo dispositivo. O tempo de run time do Direct3D tem seu próprio algoritmo de gerenciamento com base em uma técnica de prioridade menos usada recentemente. O Direct3D alterna para uma técnica de prioridade usada mais recentemente quando detecta que mais recursos do que podem coexistir na memória acessível pelo dispositivo são usados em um único quadro – entre as chamadas [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9::EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

Use o [**sinalizador D3DPOOL \_ DEFAULT**](./d3dpool.md) no momento da criação para especificar que um recurso é colocado no pool de memória mais apropriado para o conjunto de usos solicitado para o recurso especificado. Isso geralmente é memória de vídeo, incluindo memória de vídeo local e memória AGP (porta gráfica acelerada). Os recursos no pool padrão não persistem por meio de transições entre os estados perdido e operacional do dispositivo. Esses recursos devem ser liberados antes de chamar redefinição e, em seguida, devem ser re-criados.

Use o [**sinalizador D3DPOOL \_ MANAGED**](./d3dpool.md) no momento da criação para especificar um recurso gerenciado. Os recursos gerenciados persistem por meio de transições entre os estados perdido e operacional do dispositivo. Esses recursos existem tanto na memória de vídeo quanto do sistema. Um recurso gerenciado será copiado para a memória de vídeo quando for necessário durante a renderização. O dispositivo pode ser restaurado com uma chamada para [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)e esses recursos continuam funcionando normalmente sem serem recarregados com os dados. No entanto, se o dispositivo deve ser destruído e re-criado, todos os recursos devem ser re-criados.

O gerenciamento de recursos não é recomendado para recursos que mudam com alta frequência. Por exemplo, buffers de vértice e índice que são usados para percorrer um grafo de cena a cada renderização de quadro, somente geometria visível para o usuário muda a cada quadro. Como os recursos gerenciados são apoiados pela memória do sistema, as alterações constantes devem ser atualizadas na memória do sistema, o que pode causar uma degradação grave no desempenho. Para esse cenário específico, [**D3DPOOL \_ DEFAULT**](./d3dpool.md) junto com [**D3DUSAGE \_ DYNAMIC**](d3dusage.md) deve ser usado.

Outro exemplo para o qual o gerenciamento de recursos não é recomendado (e explicitamente não permitido pelo runtime) é o gerenciamento de uma textura criada com [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Se a memória usada por destinos de renderização fosse gerenciada pelo runtime, seu conteúdo teria que ser constantemente copiado para a memória do sistema durante a renderização, causando grandes penalidades de desempenho. Por esse motivo, os destinos de renderização devem ser criados no pool padrão. Se o acesso à CPU dos dados contidos em um destino de renderização for necessário, os dados deverão ser copiados para um recurso criado em [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) usando [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api)ou [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Para obter mais informações sobre o estado perdido de um dispositivo, consulte Dispositivos perdidos [(Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
