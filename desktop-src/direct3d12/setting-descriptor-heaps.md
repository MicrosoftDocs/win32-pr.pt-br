---
title: Como configurar e preencher heaps de descritores
description: Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e2fcb7143b097709cb7a3c98669a7d20331bfa9553f4eac5f2cf45a1a90797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119446"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Como configurar e preencher heaps de descritores

Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez).

-   [Definindo heaps de descritores](#setting-and-populating-descriptor-heaps)
-   [Populando heaps de descritor](#populating-descriptor-heaps)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-descriptor-heaps"></a>Definindo heaps de descritores

Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são:

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Os heaps que estão sendo definidos na lista de comandos também devem ter sido criados como sombreador visível. Há três tipos de lista de comandos: direta, pacote e computação.

Depois que um heap de descritor é definido em uma lista de comandos, as chamadas subsequentes que definem tabelas de descritores se referem ao heap do descritor atual. O estado da tabela do descritor é indefinido no início de uma lista de comandos e depois que os heaps do descritor são alterados em uma lista de comandos. A definição redundante do mesmo heap de descritor não faz com que as configurações da tabela de descritores sejam indefinidas.

Em um pacote, por outro lado, os heaps de descritor só podem ser definidos uma vez (as chamadas redundantes definindo o mesmo heap duas vezes não produzem um erro); caso contrário, o comportamento será indefinido. Os heaps de descritores definidos devem corresponder ao estado quando qualquer lista de comandos chama o pacote; caso contrário, o comportamento será indefinido. Isso permite que os pacotes herdem e editem as configurações da tabela de descritor da lista de comandos. Os agrupamentos que não alteram tabelas de descritores (herdam apenas delas) não precisam definir um heap de descritor e serão herdados apenas da lista de comandos de chamada.

Quando os heaps de descritor são definidos (usando [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), todos os heaps que estão sendo usados são definidos em uma única chamada (e todos os heaps definidos anteriormente são desdefinidos pela chamada). No máximo um heap de cada tipo listado acima pode ser definido na chamada.

## <a name="populating-descriptor-heaps"></a>Populando heaps de descritor

Depois que um aplicativo cria um heap de descritor, ele pode usar métodos no dispositivo para gerar descritores diretamente no heap ou copiar descritores de um lugar para outro.

O conteúdo inicial da memória de heap do descritor é indefinido, portanto, fazer com que a GPU ou o driver referencie a memória não inicializada para renderização possa causar resultados indefinidos, como uma redefinição do dispositivo.

Se o aplicativo configurar um heap de descritor para ser visível da CPU, a CPU poderá chamar métodos para criar descritores no heap e copiar de um local para outro (incluindo entre heaps) de uma maneira isenta e livre de threads. Se o heap tiver sido configurado como SHADER_VISIBLE, a leitura pela CPU não será permitida.



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 




