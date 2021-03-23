---
title: Visão geral dos descritores
description: Os descritores são criados por chamadas à API e identificam recursos.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548268"
---
# <a name="descriptors-overview"></a>Visão geral dos descritores

Os descritores são criados por chamadas à API e identificam recursos.

-   [Dados do descritor](#descriptor-data)
-   [Identificadores de descritor](#descriptor-handles)
-   [Descritores nulos](#null-descriptors)
-   [Descritores padrão](#default-descriptors)
-   [Tópicos relacionados](#related-topics)

## <a name="descriptor-data"></a>Dados do descritor

Um descritor é um bloco de dados relativamente pequeno que descreve totalmente um objeto para a GPU, em um formato opaco específico de GPU. Há vários tipos diferentes de descritores &mdash; renderizar exibições de destino (RTVs), visualizações de estêncil de profundidade (DSVs), exibições de recurso de sombreador (SRVs), exibições de acesso não ordenado (UAVs), exibições de buffer de constantes (CBVs) e amostras.

Os descritores variam em tamanho, dependendo do hardware da GPU. Você pode consultar o tamanho de um SRV, UAV ou CBV chamando [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). Os descritores são mostrados nesta documentação como unidades indivisívels; Aqui está um exemplo.

![SRV, cbv, UAV e amostra](images/single-descriptor.png)

Os descritores são criados por chamadas à API e incluirão informações como o recurso e mapas MIP que você deseja que o descritor contenha.

O driver não rastreia ou mantém referências a descritores, cabe ao aplicativo garantir que o tipo de descritor correto esteja em uso e que as informações sejam atuais. Há uma pequena exceção a isso; o driver inspeciona as associações de destino de renderização para garantir que as cadeias de permuta funcionem corretamente.

Os descritores de objeto não precisam ser liberados ou liberados. Os drivers não anexam nenhuma alocação à criação de um descritor. Um descritor pode, no entanto, codificar referências a outras alocações para as quais o aplicativo possui o tempo de vida. Por exemplo, um descritor para um SRV deve conter o endereço virtual do recurso D3D (por exemplo, uma textura) ao qual o SRV se refere. É responsabilidade do aplicativo verificar se ele não usa um descritor SRV quando o recurso D3D subjacente do qual ele depende foi destruído ou está sendo modificado (como está sendo declarado como não residente).

A principal maneira de usar os descritores é colocá-los em heaps de descritores, que estão fazendo backup de memória para descritores.

## <a name="descriptor-handles"></a>Identificadores de descritor

Um identificador de descritor é o endereço exclusivo do descritor. É semelhante a um ponteiro, mas é opaco, pois sua implementação é específica de hardware. O identificador é exclusivo entre heaps de descritores; portanto, por exemplo, uma matriz de identificadores pode referenciar descritores em vários heaps.

Os identificadores de CPU são para uso imediato, como copiar onde a origem e o destino precisam ser identificados. Imediatamente após o uso (por exemplo, uma chamada para [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), eles podem ser reutilizados ou seu heap subjacente pode ser Descartado.

Os identificadores de GPU não são para uso imediato &mdash; que identificam locais de uma lista de comandos, para uso no tempo de execução da GPU. Eles devem ser preservados até que qualquer lista de comandos que faça referência a eles tenha sido executada inteiramente.

Para criar um identificador de descritor para o início de um heap, depois de criar o próprio heap de descritor, chame um dos seguintes métodos:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Esses métodos retornam as seguintes estruturas:

-   [**\_Identificador do \_ descritor de CPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**\_Identificador do \_ descritor de GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Como o tamanho dos descritores varia de acordo com o hardware, para obter o incremento entre cada um deles em um heap, use:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

É seguro deslocar um local inicial com um número de incrementos, copiar identificadores e passar identificadores para chamadas de API. Não é seguro desreferenciar um identificador como se ele fosse um ponteiro de CPU válido, nem analisar os bits dentro de um identificador.

Algumas estruturas auxiliares foram adicionadas, com membros de inicialização, para facilitar o gerenciamento de identificadores.

-   [**\_Identificador do \_ descritor de CPU CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**\_Identificador do \_ descritor de GPU CD3DX12 \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descritores nulos

Ao criar descritores usando chamadas à API, os aplicativos passam nulos para o ponteiro de recurso na definição do descritor para obter o efeito de nada associado quando acessado por um sombreador.

O restante do descritor deve ser preenchido o máximo possível. Por exemplo, no caso de SRVs (exibições de recursos do sombreador), o descritor pode ser usado para distinguir o tipo de exibição é (Texture1D, Texture2D e assim por diante). Os parâmetros numéricos no descritor de exibição, como o número de mipmaps, devem ser definidos como valores que são válidos para um recurso.

Em muitos casos, há um comportamento definido para acessar um recurso não associado, como SRVs que retorna valores padrão. Eles serão respeitados ao acessar um descritor nulo, contanto que o tipo de acesso ao sombreador seja compatível com o tipo de descritor. Por exemplo, se um sombreador espera um Texture2D SRV e acessa um SRV nulo definido como um Texture1D, o comportamento é indefinido e pode resultar em redefinição do dispositivo.

Em resumo, para criar um descritor nulo, passe `null` para o parâmetro de *origem* ao criar o modo de exibição com métodos como [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview). Para o parâmetro de descrição de exibição *pDesc*, defina uma configuração que funcionaria se o recurso não fosse nulo (caso contrário, uma falha pode ocorrer em algum hardware).

Os descritores de raiz, no entanto, não devem ser definidos como NULL.

No hardware nível 1 (consulte [**camadas de hardware**](./hardware-support.md), todos os descritores associados (por meio de tabelas de descritores) devem ser inicializados, como descritores reais ou descritores nulos, mesmo que não sejam acessados pelo hardware; caso contrário, o comportamento será indefinido.

No hardware tier2, isso se aplica aos descritores CBV e UAV associados, mas não aos descritores SRV.

No hardware Tier3, não há nenhuma restrição sobre isso, desde que os descritores não inicializados nunca sejam acessados.

## <a name="default-descriptors"></a>Descritores padrão

Para criar um descritor padrão para um modo de exibição específico, passe um parâmetro de *origem* válido para o método Create View (como [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), mas passe **NULL** para o parâmetro *pDesc* . Por exemplo, se o recurso contiver 14 MIPS, o modo de exibição conterá 14 MIPS. O caso padrão cobre o mapeamento mais óbvio de um recurso para uma exibição. Isso requer que o recurso seja alocado com um nome de formato totalmente qualificado (como **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** em vez de **DXGI_FORMAT_R8G8B8A8_TYPELESS**).

Os descritores padrão não podem ser usados com uma exibição de estrutura de aceleração raytracing, porque o parâmetro de *origem* fornecido deve ser **nulo** e o local deve ser passado por meio de um d3d12_raytracing_acceleration_structure_srv [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/Windows/Win32/API/d3d12/NS-d3d12-).

## <a name="related-topics"></a>Tópicos relacionados

[Descritores](descriptors.md)