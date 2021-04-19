---
title: Interfaces principais (gráficos do Direct3D 12)
description: As interfaces a seguir são declaradas em d3d12. h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: a51e35fff74ab1d0251d64578de665ad4134a843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811986"
---
# <a name="core-interfaces"></a>Interfaces de núcleo

As interfaces a seguir são declaradas em d3d12. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Representa as alocações de armazenamento para comandos da GPU (unidade de processamento gráfico). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Uma interface da qual o [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) herda. Ele representa um conjunto ordenado de comandos que a GPU executa, ao mesmo tempo que permite que a extensão dê suporte a outras listas de comandos do que apenas aquelas para elementos gráficos (como computação e cópia). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Fornece métodos para enviar listas de comandos, sincronizar a execução da lista de comandos, instrumentar a fila de comandos e atualizar mapeamentos de bloco de recursos. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Um objeto de assinatura de comando permite que os aplicativos especifiquem o desenho indireto, incluindo o formato de buffer, o tipo de comando e as associações de recursos a serem usados. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor. Heaps de descritores contêm muitos tipos de objeto que não fazem parte de um PSO (objeto de estado de pipeline), como SRVs (exibições de recursos de sombreamento), UAVs (exibições de acesso não ordenado), CBVs (exibições de buffer de constantes) e amostras. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Representa um adaptador virtual; Ele é usado para criar alocadores de comando, listas de comandos, filas de comandos, limites, recursos, objetos de estado de pipeline, heaps, assinaturas raiz, amostras e muitos modos de exibição de recursos. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Representa um adaptador virtual e expande o intervalo de métodos fornecidos pelo [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Representa um adaptador virtual. Essa interface estende [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) para criar objetos de estado de pipeline a partir de descrições de fluxo de estado de pipeline. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Representa um adaptador virtual. Essa interface estende o [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) para dar suporte à criação de heaps de diagnóstico de uso especial na memória do sistema que persistem mesmo no caso de um cenário de falha de GPU ou remoção de dispositivo. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Representa um adaptador virtual. Essa interface estende [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Representa um adaptador virtual. Essa interface estende [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Representa um adaptador virtual. Essa interface estende [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Uma interface da qual outras interfaces principais herdam, incluindo [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)e [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Ele fornece um método para retornar ao objeto de dispositivo no qual ele foi criado. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Fornece acesso ao tempo de execução para dados de dados estendidos removidos do dispositivo (DRED com). |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Esta interface controla as configurações de DRED com (dados estendidos) removidos do dispositivo. |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Representa um limite, um objeto usado para sincronização da CPU e uma ou mais GPUs.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Representa um limite. Essa interface estende [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)e dá suporte à recuperação dos sinalizadores usados para criar o limite original.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Encapsula uma lista de comandos gráficos para renderização. Inclui APIs para instrumentação da execução da lista de comandos e para configurar e limpar o estado do pipeline. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Encapsula uma lista de comandos gráficos para renderização, estendendo o interface para dar suporte a posições de exemplo programáveis, cópias atômicas para implementar técnicas de trava tardia e teste de limites de profundidade opcionais. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Encapsula uma lista de comandos gráficos para renderização, estendendo a interface para dar suporte à gravação de valores imediatos diretamente em um buffer. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Encapsula uma lista de comandos gráficos para renderização. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Encapsula uma lista de comandos gráficos para renderização, estendendo a interface para dar suporte ao rastreamento de Ray e à renderização de passagens. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Um heap é uma abstração de alocação de memória contígua, usada para gerenciar a memória física. Esse heap pode ser usado com objetos [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) para dar suporte a recursos colocados ou recursos reservados. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Representa um retorno de chamada definido pelo aplicativo usado para ser notificado das alterações de tempo de vida de um objeto. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Representa instalações para controlar o tempo de vida de um objeto rastreado por tempo de vida. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Representa um comando meta. Um meta comando é um objeto Direct3D 12 que representa um algoritmo acelerado por fornecedores de hardware independentes (IHVs). É uma referência opaca a um gerador de comando que é implementado pelo driver. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Uma interface da qual [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) e [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) herdam. Ele fornece métodos para associar dados privados e anotar nomes de objetos. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Uma interface da qual muitas outras interfaces principais herdam. Indica que o tipo de objeto encapsula alguma quantidade de memória acessível por GPU; Mas não indica fortemente se o aplicativo pode manipular a residência do objeto.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Gerencia uma biblioteca de pipeline, em particular, carregando e recuperando PSOs individuais. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Gerencia uma biblioteca de pipeline. Essa interface estende [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) para carregar PSOs de uma descrição de fluxo de estado de pipeline. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Representa o estado de todos os sombreadores definidos atualmente, bem como determinados objetos de estado de função fixa. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Gerencia um heap de consulta. Um heap de consulta mantém uma matriz de consultas, referenciada por índices. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Encapsula uma capacidade generalizada da CPU e da GPU para ler e gravar em memória física ou heaps. Ele contém abstrações para organizar e manipular matrizes simples de dados, bem como dados multidimensionais otimizados para amostragem de sombreador. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | A assinatura raiz define quais recursos estão associados ao pipeline de gráficos. Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores precisam. Atualmente, há um gráfico e uma assinatura raiz de computação por aplicativo. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contém um método para retornar a estrutura de dados desserializada [**D3D12-raiz-Signature-desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , de uma assinatura raiz serializada versão 1,0.  |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Representa uma quantidade variável de estado de configuração, incluindo sombreadores, que um aplicativo gerencia como uma única unidade e que é dada a um driver atomicamente para processar, como compilar ou otimizar.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Fornece métodos para obter e definir as propriedades de um [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Essa interface é usada para configurar o tempo de execução para ferramentas como o PIX. Não pretendido nem tem suporte para nenhum outro cenário. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contém métodos para retornar a estrutura de dados desserializada [**D3D12-raiz-Signature-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) , de qualquer versão de uma assinatura raiz serializada.  |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de núcleo](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
* [Hierarquia de interface](interface-hierarchy.md)