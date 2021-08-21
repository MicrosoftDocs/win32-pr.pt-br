---
title: Associação de recursos
description: Associação é o processo de vinculação de objetos de recurso aos sombreadores do pipeline de gráficos.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93ca7fb75e65c58aee2b2dffbb220830e2911f2c8d7ce9186a09926fa11373f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912240"
---
# <a name="resource-binding"></a>Associação de recursos

Associação é o processo de vinculação de objetos de recurso aos sombreadores do pipeline de gráficos.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Visão geral da associação de recursos](resource-binding-flow-of-control.md) | A chave para a associação de recursos no DirectX 12 são os conceitos de um *descritor,* tabelas *de* descritor, *heaps de* descritor e uma assinatura *raiz*. |
| [Diferenças encontradas no modelo de associação do Direct3D 11](binding-model.md) | Uma das principais decisões de design por trás da associação directX12 é separá-la de outras tarefas de gerenciamento. Isso coloca alguns requisitos no aplicativo para gerenciar determinados riscos potenciais. |
| [Descritores](descriptors.md) | Descritores são a unidade principal de associação para um único recurso em D3D12. |
| [Heaps de descritores](descriptor-heaps.md) | Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor. |
| [Tabelas de descritores](descriptor-tables.md) | Uma tabela de descritor é logicamente uma matriz de descritores. |
| [Assinaturas raiz](root-signatures.md) | A assinatura raiz define quais tipos de recursos estão vinculados ao pipeline de gráficos. |
| [Consulta de funcionalidade](capability-querying.md) | Seu aplicativo pode descobrir o nível de suporte para associação de recursos e muitos outros recursos, com uma chamada para [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Associação de recursos no HLSL](resource-binding-in-hlsl.md) | Este tópico descreve alguns recursos específicos do uso do modelo de sombreador HLSL (High Level Shader Language) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) com o Direct3D 12. Todo o hardware do Direct3D 12 dá suporte ao Modelo de Sombreador 5.1, portanto, o suporte para esse modelo não depende de qual é o nível do recurso de hardware. |
| [Otimizações de UMA: texturas acessíveis por CPU e swizzling padrão](default-texture-mapping.md) | As GPUs de UMA (Arquitetura de Memória Universal) oferecem algumas vantagens de eficiência em relação a GPUs discretas, especialmente ao otimizar para dispositivos móveis. Dar acesso à CPU de recursos quando a GPU é UMA pode reduzir a quantidade de cópia que ocorre entre CPU e GPU. Embora não recomendemos que os aplicativos dêm acesso à CPU a todos os recursos em designs UMA, há oportunidades para melhorar a eficiência, dando aos recursos corretos acesso à CPU. Ao contrário das GPUs discretas, a CPU pode tecnicamente ter um ponteiro para todos os recursos que a GPU pode acessar. |
| [Carregamentos de exibição de acesso não organizado digitado](typed-unordered-access-view-loads.md) | A carga com tipo UAV (Exibição de Acesso Não Organizado) é a capacidade de um sombreador ler de um UAV com um formato [**DXGI \_ específico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) |
| [Alocação dinâmica de volumes de recursos](volume-tiled-resources.md) | Texturas de volume (3D) podem ser usadas como recursos lado a lado, notando que a resolução de blocos é tridimensional. |
| [Sub-recursos](subresources.md) | Descreve como um recurso é dividido em sub-recursos e como referenciar uma única, várias ou fatias de sub-recursos. |

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação do Direct3D 12](directx-12-programming-guide.md)
* [Tutoriais de vídeo de aprendizado avançado do DirectX: Associação de recursos no DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Gerenciamento de memória](memory-management.md)