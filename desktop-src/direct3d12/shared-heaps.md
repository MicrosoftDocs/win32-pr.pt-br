---
title: Heaps compartilhados
description: O compartilhamento é útil para arquiteturas de vários processos e multiadaptadores.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "74104199"
---
# <a name="shared-heaps"></a>Heaps compartilhados

O compartilhamento é útil para arquiteturas de vários processos e multiadaptadores.

-   [Visão geral do compartilhamento](#sharing-overview)
-   [Compartilhando heaps entre processos](#sharing-heaps-across-processes)
-   [Compartilhando heaps entre adaptadores](#sharing-heaps-across-adapters)
-   [Tópicos relacionados](#related-topics)

## <a name="sharing-overview"></a>Visão geral do compartilhamento

As heaps compartilhadas permitem duas coisas: compartilhar dados em um heap em um ou mais processos e impedindo uma opção não determinística de layout de textura indefinido para recursos colocados dentro do heap. O compartilhamento de heaps entre adaptadores também elimina a necessidade de empacotamento de CPU dos dados.

Os heaps e os recursos confirmados podem ser compartilhados. Compartilhar um recurso confirmado realmente compartilha o heap implícito junto com a descrição do recurso confirmado, de modo que uma descrição de recurso compatível pode ser mapeada para o heap de outro dispositivo.

Todos os métodos são de thread livre e herdam a semântica D3D11 existente do design de compartilhamento do identificador NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Compartilhando heaps entre processos

As heaps compartilhadas são especificadas com o \_ \_ membro compartilhado do sinalizador heap D3D12 \_ da enumeração [**\_ \_ sinalizadores de heap D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Não há suporte para heaps compartilhados em heaps acessíveis por CPU: \_ carregamento de tipo de heap D3D12 \_ \_ , \_ tipo de heap D3D12 \_ \_ READBACK e \_ tipo de heap D3D12 \_ \_ personalizado sem a propriedade de página de \_ CPU D3D12 \_ \_ \_ não \_ disponível.

A impedimento de uma escolha não determinística do layout de textura indefinido pode prejudicar significativamente os cenários de renderização adiados em algumas GPUs, portanto, não é o comportamento padrão para recursos colocados e confirmados. A renderização adiada é prejudicada em algumas arquiteturas de GPU porque layouts de textura determinísticas diminuem a largura de banda de memória efetiva obtida ao renderizar simultaneamente para várias texturas de destino de renderização do mesmo formato e tamanho. As arquiteturas de GPU estão evoluindo do aproveitamento de layouts de textura não determinísticas para dar suporte a padrões de swizzle padronizados e layouts padronizados com eficiência para renderização adiada.

Os heaps compartilhados também vêm com outros custos menores:

-   Os dados de heap compartilhados não podem ser reciclados com flexibilidade como heaps em processo devido a questões de divulgação de informações, portanto, a memória física é zero'ed com mais frequência.
-   Há uma menor sobrecarga de CPU adicional e maior uso de memória do sistema durante a criação e destruição de heaps compartilhados.

## <a name="sharing-heaps-across-adapters"></a>Compartilhando heaps entre adaptadores

Os heaps compartilhados entre os adaptadores são especificados com o \_ \_ membro do \_ adaptador cruzado do sinalizador de heap D3D12 compartilhado \_ \_ da enumeração de [**\_ \_ sinalizadores de heap D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

As heaps compartilhadas de adaptador cruzado permitem que vários adaptadores compartilhem dados sem que a CPU realize o marshaling dos dados entre eles. Embora os recursos de adaptador variáveis determinem como os adaptadores eficientes podem passar dados entre eles, a simples habilitação das cópias de GPU aumenta a largura de banda efetiva obtida. Alguns layouts de textura são permitidos em heaps de adaptador cruzado para dar suporte a um intercâmbio de dados de textura, mesmo que esses layouts de textura não tenham suporte de outra forma. Determinadas restrições podem se aplicar a essas texturas, como apenas a cópia de suporte.

O compartilhamento entre adaptadores funciona com heaps criados chamando [**ID3D12Device:: createheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Os aplicativos podem criar recursos por meio do [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). Ele também é permitido por recursos/heaps criados por [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) , mas somente para recursos de TEXTURE2D de dimensão de recurso de D3D12 de linha principal \_ \_ \_ (consulte [**D3D12 \_ Resource \_ Dimension**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). O compartilhamento entre adaptadores não funciona com [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

Para o compartilhamento entre adaptadores, todas as regras comuns de compartilhamento de recursos de fila cruzada ainda se aplicam. Os aplicativos devem emitir as barreiras apropriadas para garantir a sincronização adequada e o coerência entre os dois adaptadores. Os aplicativos devem usar limites de adaptador cruzado para coordenar o agendamento de listas de comandos enviadas a vários adaptadores. Não há nenhum mecanismo para compartilhar recursos entre adaptadores nas versões da API do D3D. Recursos compartilhados entre adaptadores só têm suporte na memória do sistema. Os recursos/heaps compartilhados entre adaptadores têm suporte em heaps padrão de tipo de heap D3D12 e heaps \_ \_ personalizados de \_ \_ \_ tipo de heap D3D12 \_ (com o pool de memória L0 e as propriedades da página de CPU de combinação de gravação). Os drivers devem ter certeza de que as operações de leitura/gravação de GPU para heaps compartilhados entre adaptadores são coerentes com outras GPUs no sistema. Por exemplo, o driver pode precisar excluir os dados de heap que residem em caches de GPU que normalmente não precisam ser liberados quando a CPU não pode acessar diretamente os dados de heap.

Os aplicativos devem restringir o uso de heaps de adaptador cruzado apenas aos cenários que exigem a funcionalidade que eles fornecem. Os heaps de adaptador cruzado estão localizados no \_ pool de memória D3D12 \_ \_ L0, que nem sempre é o que [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) sugere. Esse pool de memória não é eficiente para arquiteturas de adaptadores discretos/NUMA. E os layouts de textura mais eficientes nem sempre estão disponíveis.

As seguintes limitações também se aplicam:

-   Os sinalizadores de heap relacionados a camadas de heap devem ser \_ sinalizador de heap D3D12 \_ \_ permitir \_ todos os \_ buffers \_ e \_ texturas.
-   O \_ sinalizador de heap D3D12 \_ \_ compartilhado também deve ser definido.
-   O \_ \_ tipo de heap D3D12 \_ padrão deve ser definido ou D3D12 \_ tipo de heap \_ \_ personalizado com D3D12 \_ \_ pool de memória \_ L0 e D3D12 \_ propriedade de página de CPU \_ \_ \_ não \_ disponível deve ser definido.
-   Somente os recursos com \_ sinalizador de recurso D3D12 \_ \_ permitir \_ adaptador cruzado \_ podem ser colocados em heaps de adaptador cruzado.

Para obter mais informações sobre como usar vários adaptadores, consulte a seção [sistemas de vários adaptadores](multi-engine.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subalocação dentro de heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




