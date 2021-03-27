---
title: Níveis de recursos do Direct3D
description: Este tópico discute os níveis de recurso do Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Nível de recurso DX
- Nível de recursos do DirectX
- nível de recurso, DX
- nível de recurso, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 82667a7a2e02d675185fd65c318aeed10db79844
ms.sourcegitcommit: 85bd7112570865dd2136e0d05bd0a4132e6313ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "104008507"
---
# <a name="direct3d-feature-levels"></a>Níveis de recursos do Direct3D

Para lidar com a diversidade de placas de vídeo em máquinas novas e existentes, o Microsoft Direct3D 11 apresenta o conceito de níveis de recursos. Este tópico discute os níveis de recurso do Direct3D.

Cada placa de vídeo implementa um certo nível de funcionalidade DX (Microsoft DirectX), dependendo das GPUs (unidades de processamento gráfico) instaladas. Em versões anteriores do Microsoft Direct3D, você poderia descobrir a versão do Direct3D que a placa de vídeo implementou e programar o seu aplicativo adequadamente.

Com o Direct3D 11, é introduzido um novo paradigma chamado níveis de recursos. Um nível de recurso é um conjunto bem definido de funcionalidades de GPU. Por exemplo, o nível de recurso de 9 \_ 1 implementa a funcionalidade implementada no Microsoft Direct3D 9, que expõe os recursos dos modelos de sombreador [PS \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) e [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), enquanto o \_ nível de recurso 11 0 implementa a funcionalidade que foi implementada no Direct3D 11.

Agora, ao criar um dispositivo, você pode tentar criar um dispositivo para o nível de recurso que deseja solicitar. Se for possível criar um dispositivo, isso significa que o nível de recursos existe; caso contrário, o hardware não permite tal nível de recursos. Você pode tentar recriar um dispositivo em um nível de recursos inferior ou optar por sair do aplicativo. Para obter mais informações sobre como criar um dispositivo, consulte a função [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) .

Usando níveis de recursos, você pode desenvolver um aplicativo para o Direct3D 9, o Microsoft Direct3D 10 ou o Direct3D 11 e executá-lo em 9, 10 ou 11 hardware (com algumas exceções; por exemplo, novos 11 recursos não serão executados em um cartão 9 existente). Aqui estão algumas outras propriedades básicas dos níveis de recursos:

- Uma GPU que permite a criação de um dispositivo atende ou excede a funcionalidade desse nível de recurso.
- Um nível de recurso sempre inclui a funcionalidade dos níveis de recursos anteriores ou inferiores.
- Um nível de recurso não implica o desempenho, apenas a funcionalidade. O desempenho depende da implementação de hardware.
- Escolha um nível de recurso ao criar um dispositivo Direct3D 11.

Para obter informações sobre limitações na criação de dispositivos de tipo não-inseriais em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md).

Para ajudá-lo a decidir em que nível de recurso criar, compare os recursos para cada nível de recurso.

A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.

## <a name="formats-of-version-numbers"></a>Formatos de números de versão

Há três formatos para versões do Direct3D, modelos de sombreador e níveis de recursos.

- As versões do Direct3D usam um ponto; por exemplo, Direct3D 12,0.
- Os modelos de sombreador usam um ponto; por exemplo, o modelo de sombreador 5,1.
- Os níveis de recurso usam um sublinhado; por exemplo, nível de recurso 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_1-through-9_3"></a>Suporte a recursos para níveis de recurso 12_1 por meio de 9_3

Os recursos a seguir estão disponíveis para os níveis de recursos listados. Os títulos na linha superior são os níveis de recurso do Direct3D. Os cabeçalhos na coluna à esquerda são recursos. Consulte também [as notas de rodapé para as tabelas](#footnotes-for-the-tables).

| Nível de recurso de recurso \\ | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|
| Modelo de sombreador (D3D11) | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | v4.x | 4,0 | 2,0 (4 \_ 0 \_ nível \_ 9 \_ 3) \[ vs \_ 2 \_ a/PS \_ 2 \_ x \] <sup>5</sup> |
| Modelo de sombreador (D3D12) | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | N/D | N/D | N/D |
| [Recursos em ladrilho](tiled-resources.md) | Tier2<sup>6</sup> | Tier2<sup>6</sup> | Opcional | Opcional | Não | Não | Não |
| [Rasterização conservativa](conservative-rasterization.md) | Nível 1<sup>6</sup> | Opcional | Opcional | Não | Não | Não | Não |
| [Exibições de ordem do rasterizador](rasterizer-order-views.md) | Sim | Opcional | Opcional | Não | Não | Não | Não |
| [Filtros mín./máx.](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sim | Sim | Opcional | Não | Não | Não | Não |
| Mapear buffer padrão | Opcional | Opcional | Opcional | Opcional | Não | Não | Não |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md) | Opcional | Opcional | Opcional | Não | Não | Não | Não |
| Cargas de exibição de acesso não ordenado digitado | 18 formatos, mais opcional | 18 formatos, mais opcional | 3 formatos, mais opcionais | 3 formatos, mais opcionais | Não | Não | Não |
| [Sombreador de geometria](/previous-versions/bb205146(v=vs.85)) | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Saída de fluxo](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Sombreador DirectCompute/Compute](direct3d-11-advanced-stages-compute-shader.md) | Sim | Sim | Sim | Sim | Opcional | Opcional | N/D |
| <b>Nível de recurso de recurso \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Envoltória e sombreadores de domínio](direct3d-11-advanced-stages-tessellation.md) | Sim | Sim | Sim | Sim | Não | Não | Não |
| [Matrizes de recursos de textura](overviews-direct3d-11-resources-textures-intro.md) | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Matrizes de recursos cubemap](overviews-direct3d-11-resources-textures-intro.md) | Sim | Sim | Sim | Sim | Sim | Não | Não |
| [Compactação BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Compactação BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sim | Sim | Sim | Sim | Não | Não | Não |
| [De alfa para cobertura](./d3d10-graphics-programming-guide-blend-state.md) | Sim | Sim | Sim | Sim | Sim | Sim | Não |
| [Formatos estendidos (BGRA e assim por diante)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sim | Sim | Sim | Sim | Opcional | Opcional | Yes |
| [Formato XR High Color de 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sim | Sim | Sim | Sim | Opcional | Opcional | N/D |
| [Operações lógicas (mesclagem de saída)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Rasterização independente de destino | Sim | Sim | Sim | Não | Não | Não | Não |
| [Destino de renderização múltipla (MRT) com ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | No |
| Slots de UAV | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>Nível de recurso de recurso \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs em cada estágio | Sim | Sim | Sim | Não | Não | Não | N/D |
| [Contagem máxima de amostras forçada para renderização somente UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Compensação de buffer constante e atualizações parciais | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Sim<sup>1</sup> |
| formatos de 16 bits por pixel (BPP) | Sim | Sim | Sim | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> | Opcional<sup>1</sup> |
| Dimensão de textura máxima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensão cubemap máxima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extensão máxima do volume | 2.048 | 2.048 | 2.048 | 2.048 | 2.048 | 2.048 | 256 |
| Repetição máxima de textura | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Anisotropy máx. | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Contagem máxima de primitivas | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Índice de vértice máximo | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Máximo de Slots de entrada | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinos de renderização simultânea | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Consultas do oclusão | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| <b>Nível de recurso de recurso \\</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Separar alfa combinada | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Espelhar uma vez | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Sobrepondo elementos Vertex | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Máscaras de gravação independentes | Sim | Sim | Sim | Sim | Sim | Sim | Sim |
| Instanciação | Sim | Sim | Sim | Sim | Sim | Sim | Sim<sup>7</sup> |
| Não energia-de-2 condicionalmente<sup>3</sup> | Não | Não | Não | Não | Não | Não | Sim |
| Não energia-de-2 incondicionalmente<sup>4</sup> | Sim | Sim | Sim | Sim | Sim | Sim | Não |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Suporte a recursos para níveis de recurso 9_2 e 9_1

Os recursos a seguir estão disponíveis para os níveis de recursos listados. Os títulos na linha superior são os níveis de recurso do Direct3D. Os cabeçalhos na coluna à esquerda são recursos. Consulte também [as notas de rodapé para as tabelas](#footnotes-for-the-tables).

| Nível de recurso de recurso \\ | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modelo de sombreador (D3D11) | 2,0 (4 \_ 0 \_ nível \_ 9 \_ 1) | 2,0 (4 \_ 0 \_ nível \_ 9 \_ 1) |
| Modelo de sombreador (D3D12) | N/D | N/D |
| [Recursos em ladrilho](tiled-resources.md) | Não | Não |
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
| Destinos de renderização simultânea | 1 | 1 |
| Consultas do oclusão | Sim | Não |
| Separar alfa combinada | Sim | Não |
| Espelhar uma vez | Sim | Não |
| Sobrepondo elementos Vertex | Sim | Não |
| Máscaras de gravação independentes | Não | Não |
| Instanciação | Não | Não |
| Não energia-de-2 condicionalmente<sup>3</sup> | Sim | Sim |
| Não energia-de-2 incondicionalmente<sup>4</sup> | Não | Não |

## <a name="footnotes-for-the-tables"></a>Notas de rodapé para as tabelas

<sup>0</sup> requer o tempo de execução do Direct3D 11,3 ou Direct3D 12.

<sup>1</sup> requer o tempo de execução do Direct3D 11,1.

<sup>2</sup> o modelo de sombreador 5,0 e superior pode, opcionalmente, dar suporte a sombreadores de precisão dupla, sombreadores de precisão dupla estendida, instrução de sombreador **SAD4** e sombreadores de precisão parcial. Para determinar as opções do Shader Model 5,0 disponíveis para DirectX 11, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Algumas compatibilidades dependem de qual hardware você está executando. O modelo de sombreador 5,1 e acima só tem suporte por meio da API DirectX 12, independentemente do nível de recurso que está sendo usado. O DirectX 11 só dá suporte ao modelo de sombreador 5,0. A API DirectX 12 fica inativa apenas para o nível de recurso 11 \_ 0.

<sup>3</sup> em níveis de recursos 9 \_ 1, 9 \_ 2 e 9 \_ 3, o dispositivo de vídeo dá suporte ao uso de texturas 2D com dimensões que não são alimentadas de duas em duas condições. Primeiro, apenas um nível de mapa MIP para cada textura pode ser criado e, segundo, nenhum modo de amostra de encapsulamento para texturas é permitido (ou seja, os membros **addressexception**, **AddressV** e **AddressW** de [**D3D11 \_ Sample \_ desc**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) não podem ser definidos como [**D3D11 de \_ endereço de textura de texturização \_ \_**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)).

<sup>4</sup> nos níveis de recurso 10 \_ 0, 10 \_ 1 e 11 \_ 0, o dispositivo de vídeo dá suporte incondicionalmente ao uso de texturas 2D com dimensões que não são potências de dois.

<sup>5</sup> Vertex Shader 2a com 256 instruções, 32 registros temporários, controle de fluxo estático de profundidade 4, controle de fluxo dinâmico de profundidade 24 e D3DVS20CAPS \_ predicação. Pixel shader 2x com 512 instruções, 32 registros temporários, controle de fluxo estático de profundidade 4, controle de fluxo dinâmico de profundidade 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, D3DPS20CAPS \_ GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ predicação, D3DPS20CAPS \_ NODEPENDENTREADLIMIT e D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT.

<sup>6</sup> camadas mais altas opcionais.

<sup>7</sup> para o nível de recurso 9_3, os únicos métodos de renderização com suporte são **draw**, **DrawIndexed** e **DrawIndexInstanced**. Além disso, para o nível de recurso 9_3, a renderização de lista de pontos tem suporte apenas para renderização por meio do **draw**.

Para obter detalhes sobre o suporte de formato em diferentes níveis de recursos de hardware, consulte:

- [Suporte ao formato DXGI para hardware 12,1 de nível de recurso Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Suporte ao formato DXGI para hardware 12,0 de nível de recurso Direct3D](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Suporte ao formato DXGI para hardware 11,1 de nível de recurso Direct3D](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Suporte ao formato DXGI para hardware 11,0 de nível de recurso Direct3D](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions/ff471324(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10,1](/previous-versions/cc627091(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

* [Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)
* [Níveis de recursos de hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
