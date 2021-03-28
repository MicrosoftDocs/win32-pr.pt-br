---
title: Introdução com o estágio de Input-Assembler
description: Há algumas etapas necessárias para inicializar o estágio de IA (assembler de entrada).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366256"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Introdução com o estágio de Input-Assembler

Há algumas etapas necessárias para inicializar o estágio de IA (assembler de entrada). Por exemplo, você precisa criar recursos de buffer com os dados de vértice que o pipeline precisa, dizer ao estágio IA onde estão os buffers e que tipo de dados eles contêm, e especificar o tipo de primitivas a serem montadas dos dados.

As etapas básicas envolvidas na configuração do estágio IA, mostrada na tabela a seguir, são abordadas neste tópico.



| Etapa                                                                                    | Descrição                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Criar buffers de entrada](#create-input-buffers)                                           | Crie e inicialize buffers de entrada com dados de vértice de entrada.                                           |
| [Criar o objeto Input-Layout](#create-the-input-layout-object)                       | Defina como os dados de buffer de vértice serão transmitidos para o estágio IA usando um objeto de layout de entrada. |
| [Associar objetos ao estágio de Input-Assembler](#bind-objects-to-the-input-assembler-stage) | Associe os objetos criados (buffers de entrada e o objeto de layout de entrada) ao estágio IA.                 |
| [Especificar o tipo primitivo](#specify-the-primitive-type)                               | Identifique como os vértices serão montados em primitivos.                                          |
| [Chamar métodos Draw](#call-draw-methods)                                                 | Envie os dados associados ao estágio IA por meio do pipeline.                                             |



 

Depois de entender essas etapas, vá para [usando System-Generated valores](d3d10-graphics-programming-guide-input-assembler-stage-using.md).

## <a name="create-input-buffers"></a>Criar buffers de entrada

Há dois tipos de buffers de entrada: [buffers de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e buffers de índice. Os buffers de vértice fornecem dados de vértice para o estágio IA. Buffers de índice são opcionais; Eles fornecem índices para vértices do buffer de vértice. Você pode criar um ou mais buffers de vértice e, opcionalmente, um buffer de índice.

Depois de criar os recursos de buffer, você precisa criar um objeto de layout de entrada para descrever o layout de dados para o estágio IA e, em seguida, você precisa associar os recursos de buffer ao estágio IA. A criação e a associação de buffers não são necessárias se os sombreadores não usam buffers. Para obter um exemplo de um vértice simples e um sombreador de pixel que desenha um único triângulo, consulte [usando o estágio de Input-Assembler sem buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Para obter ajuda com a criação de um buffer de vértice, consulte [criar um buffer de vértice](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Para obter ajuda com a criação de um buffer de índice, consulte criar um buffer de índice.

## <a name="create-the-input-layout-object"></a>Criar o objeto Input-Layout

O objeto de layout de entrada encapsula o estado de entrada do estágio IA. Isso inclui uma descrição dos dados de entrada que estão associados ao estágio IA. Os dados são transmitidos para o estágio IA da memória, de um ou mais buffers de vértice. A descrição identifica os dados de entrada que são associados de um ou mais buffers de vértice e dá ao tempo de execução a capacidade de verificar os tipos de dados de entrada em relação aos tipos de parâmetro de entrada do sombreador. Essa verificação de tipo não apenas verifica se os tipos são compatíveis, mas também se cada um dos elementos que o sombreador exige está disponível nos recursos de buffer.

Um objeto de layout de entrada é criado a partir de uma matriz de descrições de elementos de entrada e um ponteiro para o sombreador compilado (consulte [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). A matriz contém um ou mais elementos de entrada; cada elemento input descreve um único elemento de dados Vertex de um único buffer de vértice. O conjunto inteiro de descrições de elementos de entrada descreve todos os elementos de dados de vértice de todos os buffers de vértices que serão associados ao estágio IA.

A descrição de layout a seguir descreve um único buffer de vértice que contém três elementos de dados de vértice:


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



Uma descrição de elemento de entrada descreve cada elemento contido por um único vértice em um buffer de vértice, incluindo tamanho, tipo, local e finalidade. Cada linha identifica o tipo de dados usando a semântica, o índice semântico e o formato de dados. Uma [semântica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) é uma cadeia de texto que identifica como os dados serão usados. Neste exemplo, a primeira linha identifica os dados de posição de 3 componentes (*XYZ*, por exemplo); a segunda linha identifica dados de textura de dois componentes (*UV*, por exemplo); e a terceira linha identifica dados normais.

Neste exemplo de uma descrição de elemento de entrada, o índice semântico (que é o segundo parâmetro) é definido como zero para todas as três linhas. O índice semântico ajuda a distinguir entre duas linhas que usam a mesma semântica. Como não há semântica semelhante neste exemplo, o índice semântico pode ser definido como seu valor padrão, zero.

O terceiro parâmetro é o *formato*. O formato (consulte [**o \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) especifica o número de componentes por elemento e o tipo de dados, que define o tamanho dos dados para cada elemento. O formato pode ser totalmente digitado no momento da criação do recurso ou você pode criar um recurso usando um **\_ formato dxgi**, que identifica o número de componentes em um elemento, mas deixa o tipo de dados indefinido.

### <a name="input-slots"></a>Slots de entrada

Os dados entram no estágio IA por meio de entradas chamadas de *Slots de entrada*, conforme mostrado na ilustração a seguir. O estágio IA tem *n* slots de entrada, que são projetados para acomodar até *n* buffers de vértices que fornecem dados de entrada. Cada buffer de vértice deve ser atribuído a um slot diferente; essas informações são armazenadas na declaração de layout de entrada quando o objeto de layout de entrada é criado. Você também pode especificar um deslocamento do início de cada buffer para o primeiro elemento no buffer a ser lido.

![Ilustração dos slots de entrada para o estágio ia](images/d3d10-ia-slots.png)

Os próximos dois parâmetros são o *slot de entrada* e o *deslocamento de entrada*. Ao usar vários buffers, você pode associá-los a um ou mais slots de entrada. O deslocamento de entrada é o número de bytes entre o início do buffer e o início dos dados.

### <a name="reusing-input-layout-objects"></a>Reutilizando Input-Layout objetos

Cada objeto de layout de entrada é criado com base em uma assinatura de sombreador; Isso permite que a API valide os elementos Input-layout-Object em relação à assinatura de entrada do sombreador para garantir que haja uma correspondência exata dos tipos e da semântica. Você pode criar um único objeto de layout de entrada para muitos sombreadores, desde que todas as assinaturas de entrada de sombreador tenham correspondência exata.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Associar objetos ao estágio de Input-Assembler

Depois de criar os recursos de buffer de vértice e um objeto de layout de entrada, você pode associá-los ao estágio IA chamando [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). O exemplo a seguir mostra a associação de um único buffer de vértice e um objeto de layout de entrada ao estágio IA:


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



A vinculação do objeto de layout de entrada requer apenas um ponteiro para o objeto.

No exemplo anterior, um único buffer de vértice é associado; no entanto, vários buffers de vértice podem ser associados por uma única chamada para [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), e o código a seguir mostra tal chamada para associar os buffers de três vértices:


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



Um buffer de índice é associado ao estágio IA chamando [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Especificar o tipo primitivo

Depois que os buffers de entrada tiverem sido associados, o estágio IA deve ser informado como montar os vértices em primitivos. Isso é feito especificando o [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) chamando [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); o código a seguir chama essa função para definir os dados como uma lista de triângulo sem adjacências:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



O restante dos tipos primitivos são listados na [**\_ \_ topologia primitiva do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Chamar métodos Draw

Depois que os recursos de entrada tiverem sido associados ao pipeline, um aplicativo chamará um método Draw para renderizar primitivos. Há vários métodos de desenho, que são mostrados na tabela a seguir; alguns buffers de índice de uso, alguns usam dados de instância, e alguns dados de reutilização do estágio de saída de streaming como entrada para o estágio de Assembler de entrada.



| Métodos Draw                                                                                  | Description                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Desenhe primitivos não indexados e não de instância.                                                            |
| [**ID3D11DeviceContext::DrawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Desenhe primitivos com instância não indexada.                                                                |
| [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Desenhe primitivos indexados e não-instância.                                                                |
| [**ID3D11DeviceContext::DrawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Desenhe primitivos indexados e com instância.                                                                    |
| [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Desenhe primitivos não indexados e não-instância de dados de entrada provenientes do estágio streaming-output. |



 

Cada método Draw renderiza um único tipo de topologia. Durante a renderização, os primitivos incompletos (aqueles sem vértices suficientes, não há índices, primitivos parciais e assim por diante) são silenciosamente descartados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de Assembler de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 