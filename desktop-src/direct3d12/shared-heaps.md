---
title: Heaps compartilhados
description: O compartilhamento é útil para arquiteturas de vários processos e vários adaptadores.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e1bc0826651334d3d137466cc34d194fb79ae4900075b9a145859c5fd37fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300807"
---
# <a name="shared-heaps"></a>Heaps compartilhados

O compartilhamento é útil para arquiteturas de vários processos e vários adaptadores.

-   [Visão geral do compartilhamento](#sharing-overview)
-   [Compartilhando heaps entre processos](#sharing-heaps-across-processes)
-   [Compartilhando heaps entre adaptadores](#sharing-heaps-across-adapters)
-   [Tópicos relacionados](#related-topics)

## <a name="sharing-overview"></a>Visão geral do compartilhamento

Os heaps compartilhados permitem duas coisas: compartilhar dados em um heap em um ou mais processos e impedir uma escolha não determinística de layout de textura indefinido para recursos colocados dentro do heap. O compartilhamento de heaps entre adaptadores também remove a necessidade de marshaling de CPU dos dados.

Os heaps e os recursos confirmados podem ser compartilhados. O compartilhamento de um recurso confirmado, na verdade, compartilha o heap implícito junto com a descrição do recurso confirmado, de forma que uma descrição de recurso compatível possa ser mapeada para o heap de outro dispositivo.

Todos os métodos têm thread livre e herdam a semântica D3D11 existente do design de compartilhamento de alça NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Compartilhando heaps entre processos

Heaps compartilhados são especificados com o membro COMPARTILHADO DO SINALIZADOR HEAP D3D12 da \_ \_ \_ enum [**D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Não há suporte para heaps compartilhados em heaps acessíveis à CPU: D3D12 \_ HEAP \_ TYPE \_ UPLOAD, D3D12 HEAP TYPE READBACK e \_ \_ \_ D3D12 HEAP TYPE CUSTOM sem A PROPRIEDADE \_ \_ \_ D3D12 \_ CPU PAGE NOT \_ \_ \_ \_ AVAILABLE.

Impedir uma escolha não determinística de layout de textura indefinido pode prejudicar significativamente os cenários de renderização adiada em algumas GPUs, portanto, não é o comportamento padrão para recursos colocados e comprometidos. A renderização adiada é prejudicada em algumas arquiteturas de GPU porque layouts de textura determinísticos diminuem a largura de banda de memória efetiva alcançada ao renderizar simultaneamente para várias texturas de destino de renderização do mesmo formato e tamanho. As arquiteturas de GPU estão evoluindo longe de aproveitar layouts de textura não determinísticos para dar suporte a padrões de swizzle padronizados e layouts padronizados com eficiência para renderização adiada.

Os heaps compartilhados também vêm com outros custos secundários:

-   Dados de heap compartilhados não podem ser reciclados tão flexíveis quanto heaps em processo devido a preocupações de divulgação de informações, portanto, a memória física é zero'ed com mais frequência.
-   Há uma pequena sobrecarga adicional de CPU e maior uso de memória do sistema durante a criação e destruição de heaps compartilhados.

## <a name="sharing-heaps-across-adapters"></a>Compartilhando heaps entre adaptadores

Heaps compartilhados entre adaptadores são especificados com o membro D3D12 HEAP FLAG SHARED CROSS ADAPTER da \_ \_ \_ \_ \_ enum [**D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Heaps compartilhados entre adaptadores permitem que vários adaptadores compartilhem dados sem que a CPU marshaling dos dados entre eles. Embora as funcionalidades de adaptadores variáveis determinem como adaptadores eficientes podem passar dados entre eles, a simples habilitação de cópias de GPU aumenta a largura de banda efetiva alcançada. Alguns layouts de textura são permitidos em heaps entre adaptadores para dar suporte a um intercâmbio de dados de textura, mesmo que esses layouts de textura não sejam suportados de outra forma. Determinadas restrições podem se aplicar a essas texturas, como apenas dar suporte à cópia.

O compartilhamento entre adaptadores funciona com heaps criados chamando [**ID3D12Device::CreateHeap.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap) Os aplicativos podem criar recursos por [**meio de CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). Ele também é permitido por recursos/heaps criados por [**CreateCommittedResource,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) mas somente para recursos de DIMENSÃO DE RECURSO TEXTURE2D D3D12 principal (consulte \_ \_ \_ [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). O compartilhamento entre adaptadores não funciona [**com CreateReservedResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

Para o compartilhamento entre adaptadores, todas as regras comuns de compartilhamento de recursos entre filas ainda se aplicam. Os aplicativos devem emitir as barreiras apropriadas para garantir a sincronização e a coerência adequadas entre os dois adaptadores. Os aplicativos devem usar cercas entre adaptadores para coordenar o agendamento de listas de comandos enviadas para vários adaptadores. Não há nenhum mecanismo para compartilhar recursos entre adaptadores entre versões da API D3D. Os recursos compartilhados entre adaptadores só têm suporte na memória do sistema. Heaps/recursos compartilhados entre adaptadores são suportados em heaps D3D12 HEAP TYPE DEFAULT e heaps PERSONALIZADOs do TIPO \_ \_ HEAP \_ D3D12 (com o pool de memória \_ \_ L0 e propriedades de página de CPU de combinação de \_ gravação). Os drivers devem ter certeza de que as operações de leitura/gravação de GPU para heaps compartilhados entre adaptadores são coerentes com outras GPUs no sistema. Por exemplo, o driver pode precisar excluir os dados de heap de residir em caches de GPU que normalmente não precisam ser liberados quando a CPU não pode acessar diretamente os dados do heap.

Os aplicativos devem limitar o uso de heaps entre adaptadores somente aos cenários que exigem a funcionalidade que eles fornecem. Os heaps entre adaptadores estão localizados em D3D12 MEMORY POOL L0, que nem sempre é o \_ \_ que \_ [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) sugere. Esse pool de memória não é eficiente para arquiteturas de adaptador NUMA/discretos. Além disso, os layouts de textura mais eficientes nem sempre estão disponíveis.

As seguintes limitações também se aplicam:

-   Os sinalizadores de heap relacionados às camadas de heap devem ser SINALIZADOR DE HEAP D3D12 \_ \_ PERMITIR TODOS OS \_ \_ \_ BUFFERS E \_ \_ TEXTURAS.
-   O SINALIZADOR DE HEAP D3D12 \_ SHARED também deve ser \_ \_ definido.
-   D3D12 HEAP TYPE DEFAULT deve ser definido ou \_ \_ \_ D3D12 HEAP TYPE CUSTOM com \_ \_ \_ D3D12 \_ MEMORY POOL \_ \_ L0 e D3D12 \_ A \_ \_ \_ \_ PROPRIEDADE DE PÁGINA DA CPU NÃO DISPONÍVEL deve ser definida.
-   Somente recursos com O SINALIZADOR DE RECURSO D3D12 ALLOW CROSS ADAPTER podem \_ \_ ser colocados em \_ \_ \_ heaps entre adaptadores.

Para obter mais informações sobre como usar vários adaptadores, consulte a seção [Sistemas de vários adaptadores.](multi-engine.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subalocação em heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




