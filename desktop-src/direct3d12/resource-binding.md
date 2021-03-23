---
title: Associação de recursos
description: Binding é o processo de vinculação de objetos de recursos aos sombreadores do pipeline de gráficos.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548277"
---
# <a name="resource-binding"></a>Associação de recursos

Binding é o processo de vinculação de objetos de recursos aos sombreadores do pipeline de gráficos.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Visão geral da Associação de recursos](resource-binding-flow-of-control.md) | A chave para a associação de recursos no DirectX 12 são os conceitos de um *descritor*, *tabelas de descritores*, *heaps de descritores* e uma *assinatura de raiz*. |
| [Diferenças no modelo de associação do Direct3D 11](binding-model.md) | Uma das principais decisões de design por trás da Associação DirectX12 é separá-la de outras tarefas de gerenciamento. Isso coloca alguns requisitos no aplicativo para gerenciar determinados riscos potenciais. |
| [Descritores](descriptors.md) | Os descritores são a unidade primária de associação para um único recurso no D3D12. |
| [Heaps de descritores](descriptor-heaps.md) | Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor. |
| [Tabelas de descritores](descriptor-tables.md) | Uma tabela de descritores é logicamente uma matriz de descritores. |
| [Assinaturas raiz](root-signatures.md) | A assinatura raiz define quais tipos de recursos estão associados ao pipeline de gráficos. |
| [Consulta de funcionalidade](capability-querying.md) | Seu aplicativo pode descobrir o nível de suporte para associação de recursos e muitos outros recursos, com uma chamada para [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Associação de recursos em HLSL](resource-binding-in-hlsl.md) | Este tópico descreve alguns recursos específicos do usando o [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (sombreamento de alto nível) 5,1 com o Direct3D 12. Todo o hardware do Direct3D 12 dá suporte ao modelo de sombreador 5,1, portanto, o suporte para esse modelo não depende do nível de recurso de hardware. |
| [Otimizações de uma: texturas acessíveis de CPU e swizzle padrão](default-texture-mapping.md) | As GPUs da arquitetura de memória universal (a) oferecem algumas vantagens de eficiência em relação a GPUs discretas, especialmente ao otimizar para dispositivos móveis. Conceder acesso à CPU de recursos quando a GPU é uma pode reduzir a quantidade de cópia que ocorre entre a CPU e a GPU. Embora não recomendemos que os aplicativos insistam no acesso à CPU a todos os recursos em designs de uma, há oportunidades de melhorar a eficiência fornecendo o acesso à CPU de recursos corretos. Ao contrário de GPUs discretas, a CPU pode tecnicamente ter um ponteiro para todos os recursos que a GPU pode acessar. |
| [Cargas de exibição de acesso não ordenado digitado](typed-unordered-access-view-loads.md) | A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico. |
| [Recursos de sublado do volume](volume-tiled-resources.md) | Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional. |
| [Sub-recursos](subresources.md) | Descreve como um recurso é dividido em subrecursos e como fazer referência a uma única, várias ou fatia de subrecursos. |

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação do Direct3D 12](directx-12-programming-guide.md)
* [Tutoriais de vídeo do DirectX Advanced Learning: Associação de recursos no DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Gerenciamento de memória](memory-management.md)