---
description: O desempenho das operações de processamento de vértice, incluindo a transformação e a iluminação, depende muito de onde o buffer de vértice existe na memória e que tipo de dispositivo de renderização está sendo usado.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Tipos de dispositivo e requisitos de processamento de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500398"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Tipos de dispositivo e requisitos de processamento de vértice (Direct3D 9)

O desempenho das operações de processamento de vértice, incluindo a transformação e a iluminação, depende muito de onde o buffer de vértice existe na memória e que tipo de dispositivo de renderização está sendo usado. Os aplicativos controlam a alocação de memória para buffers de vértice quando eles são criados. Quando o \_ sinalizador de memória D3DPOOL SYSTEMMEM é definido, o buffer de vértice é criado na memória do sistema. Quando o \_ sinalizador de memória padrão D3DPOOL é usado, o driver de dispositivo determina onde a memória para o buffer de vértice é melhor alocada, geralmente conhecida como memória de driver ideal. Driver-a memória ideal pode ser memória de vídeo local, memória de vídeo não local ou memória do sistema.

Definir a \_ constante D3DUSAGE SOFTWAREPROCESSING com [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) habilita o processamento de vértice de software nos dados do buffer de vértice. Esse sinalizador é necessário para o processamento de vértice de software no modo misto. O sinalizador não pode ser usado para o modo de processamento de vértice de hardware. Os buffers de vértice usados com o processamento de vértice de software incluem o seguinte:

-   Todos os fluxos de entrada para [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).
-   Todos os fluxos de entrada para [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

O raciocínio que você usa para determinar o sistema de local de memória ou o driver ideal-para buffers de vértice é o mesmo que para texturas. O processamento de vértices, incluindo a transformação e a iluminação, em hardware funciona melhor quando os buffers de vértice são alocados no driver-ideal de memória, enquanto o processamento de vértice de software funciona melhor com buffers de vértice alocados na memória do sistema. Para texturas, a rasterização de hardware funciona melhor quando as texturas são alocadas na memória ideal para o driver, enquanto a rasterização de software funciona melhor com texturas de memória do sistema.

O Microsoft Direct3D 9 dá suporte ao processamento autônomo de vértices, sem processar nenhum primitivo com o método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) . Esse processamento de vértice autônomo é sempre executado em software no processador do host. Por isso, os buffers de vértice usados como fontes definidas com [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api) devem ser criados com o \_ sinalizador D3DUSAGE SOFTWAREPROCESSING. A funcionalidade fornecida por **IDirect3DDevice9::P rocessvertices** é idêntica à dos métodos [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) ao usar o processamento de vértice de software.

Se seu aplicativo executa seu próprio processamento de vértice e passa os vértices transformados, acesos e recortados para métodos de renderização, o aplicativo pode gravar vértices diretamente em um buffer de vértice alocado na memória do driver-ideal. Essa técnica impede uma operação de cópia redundante mais tarde. Observe que essa técnica não funcionará bem se o seu aplicativo lê dados de volta de um buffer de vértice, pois as operações de leitura realizadas pelo host do driver-a memória ideal podem ser muito lentas. Portanto, se seu aplicativo precisar ler durante o processamento ou gravar dados no buffer incorretamente, um buffer de vértice da memória do sistema será uma opção melhor.

Ao usar os recursos de processamento de vértice de Direct3D (passando vértices não transformados para métodos de renderização de buffer de vértice), o processamento pode ocorrer em hardware ou software, dependendo do tipo de dispositivo e dos sinalizadores de criação de dispositivo. É recomendável que os buffers de vértice sejam alocados no pool D3DPOOL \_ padrão para melhor desempenho em praticamente todos os casos. Quando um dispositivo está usando o processamento de vértice de hardware, há várias otimizações adicionais que podem ser feitas com base nos sinalizadores D3DUSAGE \_ dinâmico e D3DUSAGE \_ WRITEONLY. Consulte IDirect3DDevice9:: CreateVertexBuffer para obter mais informações sobre como usar esses sinalizadores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
