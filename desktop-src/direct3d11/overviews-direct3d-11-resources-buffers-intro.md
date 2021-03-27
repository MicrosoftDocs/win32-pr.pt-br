---
title: Introdução aos buffers no Direct3D 11
description: Um recurso de buffer é uma coleção de dados completamente tipados, agrupados em elementos.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- buffer de constantes, o que é
- buffer de vértice, o que é
- buffer de índice, o que é
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294165"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Introdução aos buffers no Direct3D 11

Um recurso de buffer é uma coleção de dados completamente tipados, agrupados em elementos. É possível usar buffers para armazenar uma ampla variedade de dados, incluindo vetores de posição, vetores normais, coordenadas de textura em um buffer de vértice, índices em um buffer de índice ou estado do dispositivo. Um elemento de buffer é composto de 1 a 4 componentes. Elementos de buffer podem incluir valores de dados de pacote (como valores de superfície R8G8B8A8), inteiros de 8 bits únicos ou quatro valores de ponto flutuante de 32 bits.

Um buffer é criado como um recurso não estruturado. Como ele não é estruturado, um buffer não pode conter níveis de mipmap, não pode ser filtrado quando lido e não pode conter várias amostras.

## <a name="buffer-types"></a>Tipos de buffer

Os tipos de recursos de buffer seguintes são compatíveis com Direct3D 11. Todos os tipos de buffer são encapsulados pela interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) .

-   [Buffer de vértice](#vertex-buffer)
-   [Buffer de índice](#index-buffer)
-   [Buffer de constantes](#constant-buffer)

### <a name="vertex-buffer"></a>Buffer de vértice

Um buffer de vértice contém os dados de vértice usados para definir sua geometria. Dados de vértice incluem coordenadas de posição, dados de cor, dados de coordenadas de textura, dados normais e assim por diante.

O exemplo mais simples de um buffer de vértice é aquele que contém apenas dados de posição. Ele pode ser visualizado como na ilustração a seguir.

![ilustração de um buffer de vértices que contém dados de posição](images/d3d10-resources-single-element-vb2.png)

Com mais frequência, um buffer de vértices contém todos os dados necessários para especificar totalmente vértices 3D. Um exemplo disso pode ser um buffer de vértices que contém coordenadas de posição, normais e de textura por vértice. Esses dados geralmente são organizados como conjuntos de elementos por vértice, conforme mostrado na ilustração a seguir.

![ilustração de um buffer de vértices que contém dados de posição, normais e de textura](images/d3d10-vertex-buffer-element.png)

Esse buffer de vértice contém dados por vértice; cada vértice armazena três elementos (posição, normal e coordenadas de textura). A posição e o normal são cada um normalmente especificado usando floats de 3 32 bits ( \_ float do formato dxgi \_ R32G32B32 \_ ) e as coordenadas de textura usando floats de 2 32 bits ( \_ formato dxgi \_ R32G32 \_ float).

Para acessar os dados em um buffer de vértice, você precisa saber qual vértice acessar, além dos seguintes parâmetros de buffer adicionais:

-   Deslocamento -o número de bytes desde o início do buffer para os dados para o primeiro vértice. Você pode especificar o deslocamento usando o método [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) .
-   BaseVertexLocation -o número de bytes do deslocamento até o primeiro vértice usado pela chamada de desenho apropriada.

Antes de criar um buffer de vértice, você precisa definir seu layout criando uma interface [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) ; Isso é feito chamando o método [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) . Depois que o objeto de layout de entrada é criado, você pode associá-lo ao estágio de Assembler de entrada chamando o [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).

Para criar um buffer de vértice, chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Buffer de índice

Buffers de índice contêm deslocamentos de inteiros em buffers de vértice e são usados para renderizar primitivas de forma mais eficiente. Um buffer de índice contém um conjunto sequencial de índices de 16 ou 32 bits; cada índice é usado para identificar um vértice em um buffer de vértices. Um buffer de índice pode ser visualizado como na ilustração a seguir.

![ilustração de um buffer de índice](images/d3d10-index-buffer.png)

Os índices sequenciais armazenados em um buffer de índice estão localizados com os seguintes parâmetros:

-   Deslocamento - o número de bytes do endereço base do buffer de índice. O deslocamento é fornecido para o método [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) .
-   StartIndexLocation-especifica o primeiro elemento de buffer de índice do endereço base e o deslocamento fornecido em [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer). O local inicial é fornecido para o método [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) ou [**ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) e representa o primeiro índice a ser renderizado.
-   IndexCount -o número de índices para renderizar. O número é fornecido para o método [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Início do buffer de índice = endereço base do buffer de índice + deslocamento (bytes) + \* elementos StartIndexLocation (bytes);

Nesse cálculo, ElementSize é o tamanho de cada elemento de buffer de índice, que é dois ou quatro bytes.

Para criar um buffer de índice, chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Buffer constante

Um buffer constante permite que você forneça com eficiência dados constantes do sombreador no pipeline. Você pode usar um buffer constante para armazenar os resultados do estágio de fluxo de saída. Conceitualmente, um buffer constante parece muito com um buffer de vértice de elemento único, conforme mostrado na ilustração a seguir.

![ilustração de um buffer constante de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento armazena uma constante de 1 a 4 componentes determinada pelo formato dos dados armazenados. Para criar um buffer de sombreador-constante, chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e especifique o membro de **\_ \_ \_ buffer constante de associação D3D11** do tipo enumerado de [**\_ \_ sinalizador de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Um buffer de constantes só pode usar um único sinalizador de ligação (**\_ \_ \_ buffer constante de associação de D3D11**), que não pode ser combinado com nenhum outro sinalizador de ligação. Para associar um buffer de sombreador-constante ao pipeline, chame um dos seguintes métodos: [**ID3D11DeviceContext:: GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**ID3D11DeviceContext::P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)ou [**ID3D11DeviceContext:: VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Para ler um buffer de sombreador-constante de um sombreador, use uma função de carga HLSL (por exemplo, [**Load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)). Cada estágio de sombreador permite até 15 buffers constantes de sombreador; cada buffer pode manter até 4.096 constantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 