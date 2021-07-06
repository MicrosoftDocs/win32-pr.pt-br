---
title: Níveis de recursos do Direct3D
description: Este tópico discute os níveis de recursos do Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Nível de recurso DX
- Nível de recursos do DirectX
- nível de recurso, DX
- nível de recurso, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 9c4717d743e50e91376e57e5d13acbe2cfae41d8
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282465"
---
# <a name="direct3d-feature-levels"></a>Níveis de recursos do Direct3D

> [!NOTE]
> **Algumas informações relacionam-se ao produto de pré-lançamento, o qual poderá ser substancialmente modificado antes do lançamento comercial. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.**

Para lidar com a diversidade de placas de vídeo em máquinas novas e existentes, o Microsoft Direct3D 11 apresenta o conceito de níveis de recursos. Este tópico discute os níveis de recursos do Direct3D.

Cada placa de vídeo implementa um determinado nível de funcionalidade do Microsoft DirectX (DX), dependendo das GPUs (unidades de processamento gráfico) instaladas. Em versões anteriores do Microsoft Direct3D, você poderia descobrir a versão do Direct3D que a placa de vídeo implementou e programar o seu aplicativo adequadamente.

Com o Direct3D 11, um novo paradigma é introduzido chamado níveis de recurso. Um nível de recurso é um conjunto bem definido de funcionalidades de GPU. Por exemplo, o nível de recurso 9 1 implementa a funcionalidade implementada no Microsoft Direct3D 9, que expõe os recursos dos modelos de sombreador \_ [ps \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) e [ \_ 2 \_ x,](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md)enquanto o nível de recurso 11 0 implementa a funcionalidade implementada no \_ Direct3D 11.

Agora, ao criar um dispositivo, você pode tentar criar um dispositivo para o nível de recurso que deseja solicitar. Se for possível criar um dispositivo, isso significa que o nível de recursos existe; caso contrário, o hardware não permite tal nível de recursos. Você pode tentar recriar um dispositivo em um nível de recursos inferior ou optar por sair do aplicativo. Para obter mais informações sobre como criar um dispositivo, consulte a [**função D3D11CreateDevice.**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice)

Usando níveis de recurso, você pode desenvolver um aplicativo para Direct3D 9, Microsoft Direct3D 10 ou Direct3D 11 e, em seguida, executar em hardware 9, 10 ou 11 (com algumas exceções; por exemplo, novos 11 recursos não serão executados em um cartão 9 existente). Aqui estão algumas outras propriedades básicas dos níveis de recurso:

- Uma GPU que permite que um dispositivo seja criado atende ou excede a funcionalidade desse nível de recurso.
- Um nível de recurso sempre inclui a funcionalidade dos níveis de recursos anteriores ou inferiores.
- Um nível de recurso não implica desempenho, apenas funcionalidade. O desempenho depende da implementação de hardware.
- Escolha um nível de recurso ao criar um dispositivo Direct3D 11.

Para obter informações sobre limitações ao criar dispositivos não de tipoware em determinados níveis de recurso, consulte Limitações ao [criar DISPOSITIVOs DE DISTORÇÃO e Referência.](overviews-direct3d-11-devices-limitations.md)

Para ajudá-lo a decidir com qual nível de recurso projetar, compare os recursos para cada nível de recurso.

A seção [Referência 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre como vários métodos [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) se comportam em vários níveis de recurso 10Level9.

## <a name="formats-of-version-numbers"></a>Formatos de números de versão

Há três formatos para versões do Direct3D, modelos de sombreador e níveis de recursos.

- As versões do Direct3D usam um ponto; por exemplo, Direct3D 12.0.
- Os modelos de sombreador usam um ponto; por exemplo, modelo de sombreador 5.1.
- Os níveis de recurso usam um sublinhado; por exemplo, nível de recurso 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>Suporte a recursos para níveis de recurso 12_2 a 9_3

Os recursos a seguir estão disponíveis para os níveis de recursos listados. Os títulos na linha superior são níveis de recurso direct3D. Os títulos na coluna à esquerda são recursos. Consulte também [Notas de rodapé para as tabelas](#footnotes-for-the-tables).

| Nível \\ de recurso do recurso | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| Modelo de sombreador (D3D11) | N/D | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 4.x | 4,0 | 2.0 (4 \_ 0 \_ nível \_ 9 \_ 3) \[ vs \_ 2 \_ a/ps \_ 2 x \_ \] <sup>5</sup> |
| Modelo de sombreador (D3D12) | 6.5 | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | N/D | N/D | N/D |
| [Recursos lado a lado](tiled-resources.md) | Camada 3 | Camada<sup>2 6</sup> | Camada<sup>2 6</sup> | Opcional | Opcional | Não | Não | Não |
| [Rasterização conservativa](conservative-rasterization.md) | Camada 3 | Camada<sup>1 6</sup> | Opcional | Opcional | Não | Não | Não | Não |
| [Exibições de ordem do rasterizador](rasterizer-order-views.md) | Sim | Sim | Opcional | Opcional | Não | Não | Não | Não |
| [Filtros mínimos/máximos](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sim | Sim | Sim | Opcional | Não | Não | Não | Não |
| Mapear buffer padrão | N/D | Opcional | Opcional | Opcional | Opcional | Não | Não | Não |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md) | Opcional | Opcional | Opcional | Opcional | Não | Não | Não | Não |
| Carregamentos de exibição de acesso não organizado digitado | 18 formatos, mais opcionais | 18 formatos, mais opcionais | 18 formatos, mais opcionais | Três formatos, mais opcionais | Três formatos, mais opcionais | Não | Não | Não |
| [Sombreador de geometria](/previous-versions/bb205146(v=vs.85)) | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Stream Out](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [DirectCompute/Sombreador de Computação](direct3d-11-advanced-stages-compute-shader.md) | Sim | Sim | Sim | Sim | Sim | Opcional | Opcional | N/D |
| <b>Nível \\ de recurso do recurso</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Sombreadores de chassi e domínio](direct3d-11-advanced-stages-tessellation.md) | Sim | Sim | Sim | Sim | Sim | Não | Não | Não |
| [Matrizes de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Matrizes de recursos cubemap](overviews-direct3d-11-resources-textures-intro.md) | Sim | Sim | Sim | Sim | Sim | Sim | Não | Não |
| [Compactação BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Compactação BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sim | Sim | Sim | Sim | Sim | Não | Não | Não |
| [De alfa para cobertura](./d3d10-graphics-programming-guide-blend-state.md) | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Formatos estendidos (BGRA e assim por diante)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sim | Sim | Sim | Sim | Sim | Opcional | Opcional | Sim |
| [Formato XR High Color de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sim | Sim | Sim | Sim | Sim | Opcional | Opcional | N/D |
| [Operações lógicas (mesclagem de saída)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sim | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Não |
| Rasterização independente de destino | Sim | Sim | Sim | Sim | Não | Não | Não | Não |
| [Destino de renderização múltipla (MRT) com ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sim | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Não |
| Slots de UAV | Em camadas<sup>9</sup> | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>Nível de recurso de recurso \\</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs em cada estágio | Sim | Sim | Sim | Sim | Não | Não | Não | N/D |
| [Contagem máxima de amostras forçada para renderização somente UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Deslocamento de buffer constante e atualizações parciais | Sim | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Sim<sup>1</sup> |
| Formatos de 16 bits por pixel (bpp) | Sim | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensão de textura máxima | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensão Max Cubemap | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extensão máxima do volume | 2.048 | 2.048 | 2.048 | 2.048 | 2.048 | 2.048 | 2.048 | 256 |
| Repetição máxima de textura | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Máximo de Anisoção | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Contagem máxima de primitivos | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Índice máximo de vértice | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Máximo de slots de entrada | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinos de renderização simultâneos | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Consultas de oclusão | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| <b>Nível \\ de recurso do recurso</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Combinação alfa separada | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Espelhar uma vez | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Sobrepondo elementos de vértice | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Máscaras de Gravação Independentes | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Instanciação | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim<sup>7</sup> |
| Nãopowers-of-2<sup>condicionalmente 3</sup> | Não | Não | Não | Não | Não | Não | Não | Sim |
| Nonpowers-of-2 incondicionalmente<sup>4</sup> | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Não |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Suporte a recursos para os níveis de recurso 9_2 e 9_1

Os recursos a seguir estão disponíveis para os níveis de recursos listados. Os títulos na linha superior são níveis de recurso direct3D. Os títulos na coluna à esquerda são recursos. Consulte também [Notas de rodapé para as tabelas](#footnotes-for-the-tables).

| Nível \\ de recurso do recurso | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modelo de sombreador (D3D11) | 2.0 (4 \_ 0 \_ nível \_ 9 \_ 1) | 2.0 (4 \_ 0 \_ nível \_ 9 \_ 1) |
| Modelo de sombreador (D3D12) | N/D | N/D |
| [Recursos lado a lado](tiled-resources.md) | Não | Não |
| [Rasterização conservativa](conservative-rasterization.md) | Não | Não |
| [Exibições de ordem do rasterizador](rasterizer-order-views.md) | Não | Não |
| [Filtros mín./máx.](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Não | Não |
| Mapear buffer padrão | Não | Não |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md) | Não | Não |
| Cargas de exibição de acesso não ordenado digitado | Não | Não |
| [Sombreador de geometria](/previous-versions/bb205146(v=vs.85)) | Não | Não |
| [Saída de fluxo](./d3d10-graphics-programming-guide-output-stream-stage.md) | Não | Não |
| [Sombreador DirectCompute/Compute](direct3d-11-advanced-stages-compute-shader.md) | N/D | N/D |
| [Envoltória e sombreadores de domínio](direct3d-11-advanced-stages-tessellation.md) | Não | Não |
| [Matrizes de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | Não | Não |
| [Matrizes de recursos cubemap](overviews-direct3d-11-resources-textures-intro.md) | Não | Não |
| [Compactação BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Não | Não |
| <b>Nível de recurso de recurso \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compactação BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Não | Não |
| [De alfa para cobertura](./d3d10-graphics-programming-guide-blend-state.md) | Não | Não |
| [Formatos estendidos (BGRA e assim por diante)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sim | Sim |
| [Formato XR High Color de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/D | N/D |
| [Operações lógicas (mesclagem de saída)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Não | Não |
| Rasterização independente de destino | Não | Não |
| [Destino de renderização múltipla (MRT) com ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Não | Não |
| Slots de UAV | N/D | N/D |
| UAVs em cada estágio | N/D | N/D |
| [Contagem máxima de amostras forçada para renderização somente UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/D | N/D |
| Compensação de buffer constante e atualizações parciais | Sim<sup>1</sup> | Sim<sup>1</sup> |
| formatos de 16 bits por pixel (BPP) | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensão de textura máxima | 2.048 | 2.048 |
| Dimensão cubemap máxima | 512 | 512 |
| Extensão máxima do volume | 256 | 256 |
| Repetição máxima de textura | 2.048 | 128 |
| <b>Nível de recurso de recurso \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Anisotropy máx. | 16 | 2 |
| Contagem máxima de primitivas | 1048575 | 65535 |
| Índice de vértice máximo | 1048575 | 65534 |
| Máximo de Slots de entrada | 16 | 16 |
| Destinos de renderização simultâneos | 1 | 1 |
| Consultas de oclusão | Sim | Não |
| Combinação alfa separada | Sim | Não |
| Espelhar uma vez | Sim | Não |
| Sobrepondo elementos de vértice | Sim | Não |
| Máscaras de Gravação Independentes | Não | Não |
| Instanciação | Não | Não |
| Nãopowers-of-2<sup>condicionalmente 3</sup> | Sim | Sim |
| Nonpowers-of-2 incondicionalmente<sup>4</sup> | Não | Não |

## <a name="footnotes-for-the-tables"></a>Notas de rodapé para as tabelas

<sup>0</sup> Requer o runtime direct3D 11.3 ou Direct3D 12.

<sup>1</sup> Requer o runtime do Direct3D 11.1.

<sup>2</sup> O modelo de sombreador 5.0 e superior pode opcionalmente dar suporte a sombreadores de precisão dupla, sombreadores de precisão dupla estendidos, a instrução **sombreador SAD4** e sombreadores de precisão parcial. Para determinar as opções do modelo de sombreador 5.0 que estão disponíveis para o DirectX 11, chame [**ID3D11Device::CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Alguma compatibilidade depende de qual hardware você está executando. O modelo de sombreador 5.1 e superior só tem suporte por meio da API do DirectX 12, independentemente do nível de recurso que está sendo usado. O DirectX 11 dá suporte apenas ao modelo de sombreador 5.0. A API do DirectX 12 só vai para o nível de recurso 11 \_ 0.

<sup>3</sup> Nos níveis de recurso 9 1, 9 2 e 9 3, o dispositivo de exibição dá suporte ao uso de \_ \_ texturas 2D com dimensões que não são potências de dois em duas \_ condições. Primeiro, apenas um nível de mapa MIP para cada textura pode ser criado e, em segundo lugar, nenhum modo de exemplo de wrap para texturas é permitido (ou seja, os membros **AddressU,** **AddressV** e **AddressW** do [**D3D11 \_ SAMPLER \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) não podem ser definidos como [**D3D11 \_ TEXTURE ADDRESS \_ \_ WRAP**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)).

<sup>4</sup> Nos níveis de recurso 10 \_ 0, 10 1 e 11 0, o dispositivo de exibição dá suporte incondicional ao uso de \_ texturas 2D com dimensões que não são potências de \_ dois.

<sup>5</sup> Sombreador de vértice 2a com 256 instruções, 32 registros temporários, controle de fluxo estático de profundidade 4, controle de fluxo dinâmico de profundidade 24 e D3DVS20CAPS \_ PREDICATION. Sombreador de pixel 2x com 512 instruções, 32 registros temporários, controle de fluxo estático de profundidade 4, controle de fluxo dinâmico de profundidade 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, \_ D3DPS20CAPS GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ PREDICATION, D3DPS20CAPS \_ NODEPENDENTREADLIMIT e D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT.

<sup>6</sup> Camadas superiores opcionais.

<sup>7</sup> Para o Nível de Recurso 9_3, os únicos métodos de renderização com suporte são **Draw**, **DrawIndexed** e **DrawIndexInstanced**. Além disso, para o Nível de Recurso 9_3, a renderização da lista de pontos tem suporte apenas para renderização por meio do **Draw**.

<sup>8</sup> Requer o runtime do Direct3D 12.

<sup>9</sup> Na API do Direct3D 12, há limites no número de descritores em um heap CBV/SRV/UAV. Consulte [Camadas de hardware para](/windows/win32/direct3d12/hardware-support) obter detalhes. Separadamente, há um limite no número de UAVs em todas as tabelas de descritor em todos os estágios, que se baseia na camada de [associação de recursos](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support).

Para obter detalhes sobre o suporte ao formato em diferentes níveis de recursos de hardware, consulte:

- [Suporte ao formato DXGI para hardware de nível de recurso 12.1 do Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Suporte ao formato DXGI para hardware de nível de recurso 12.0 do Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Suporte ao formato DXGI para hardware de nível de recurso 11.1 do Direct3D](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Suporte ao formato DXGI para hardware de nível de recurso 11.0 do Direct3D](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions/ff471324(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10.1](/previous-versions/cc627091(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

* [Direct3D 11 no hardware de nível baixo](overviews-direct3d-11-devices-downlevel.md)
* [Níveis de recursos de hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
