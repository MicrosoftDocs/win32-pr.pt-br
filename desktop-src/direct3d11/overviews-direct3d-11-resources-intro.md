---
title: Introdução a um recurso no Direct3D 11
description: Este tópico apresenta recursos do Direct3D, como buffers e texturas.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb466883991795a66eec0ba1b99f5c989fa33c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366343"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Introdução a um recurso no Direct3D 11

Os recursos são os blocos de construção da sua cena. Eles contêm a maioria dos dados que o Direct3D usa para interpretar e renderizar sua cena. Os recursos são áreas na memória que podem ser acessadas pelo pipeline do Direct3D. Os recursos contêm os seguintes tipos de dados: Geometry, textures, dados do sombreador. Este tópico apresenta recursos do Direct3D, como buffers e texturas.

Você pode criar recursos que são fortemente tipados ou não Type; Você pode controlar se os recursos têm acesso de leitura e gravação; Você pode tornar os recursos acessíveis somente à CPU, à GPU ou a ambos. Até 128 recursos podem estar ativos para cada estágio do pipeline.

O Direct3D garante para retornar zero para qualquer recurso que seja acessado fora dos limites.

O ciclo de vida de um recurso do Direct3D é:

-   Crie um recurso usando um dos métodos Create da interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .
-   Associe um recurso ao pipeline usando um contexto e um dos métodos set da interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .
-   Desaloque um recurso chamando o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) da interface de recurso.

Esta seção contém os seguintes tópicos:

-   [Digitação forte versus fraca](#strong-vs-weak-typing)
-   [Exibições de recursos](#resource-views)
-   [Exibições brutas de buffers](#raw-views-of-buffers)
-   [Tópicos relacionados](#related-topics)

## <a name="strong-vs-weak-typing"></a>Digitação forte versus fraca

Há duas maneiras de especificar totalmente o layout (ou volume de memória) de um recurso:

-   Tipado – especifique totalmente o tipo quando o recurso é criado.
-   Sem tipo – especifique totalmente o tipo quando o recurso estiver associado ao pipeline.

Criar um recurso totalmente com tipo restringe o recurso ao formato com o qual ele foi criado. Isso permite que o tempo de execução otimize o acesso, especialmente se o recurso for criado com sinalizadores indicando que ele não pode ser mapeado pelo app. Os recursos criados com um tipo específico não podem ser reinterpretados usando o mecanismo de exibição, a menos que o recurso tenha sido criado com o sinalizador de associação do D3D10 \_ DDI \_ \_ presente. Se \_ \_ a associação de DDI d3d10 \_ presente estiver definida, as exibições de recurso de destino de renderização ou sombreador poderão ser criadas nesses recursos usando qualquer um dos membros totalmente tipados da família apropriada, mesmo que o recurso original tenha sido criado como totalmente digitado.

Em um tipo menos recurso, o tipo de dados é desconhecido quando o recurso é criado pela primeira vez. O aplicativo deve escolher entre os formatos de tipo menos disponíveis (consulte o [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Você deve especificar o tamanho da memória a alocar e se o tempo de execução precisará gerar as subtexturas em mipmap. No entanto, o formato de dados exato (se a memória será interpretada como números inteiros, valores de ponto flutuante, inteiros não assinados etc.) não é determinado até que o recurso seja associado ao pipeline com uma [exibição de recurso](#resource-views). Como o formato de textura permanece flexível até a textura ser associada ao pipeline, o recurso será referido como armazenamento com tipo fraco. O armazenamento com tipo fraco tem a vantagem de que pode ser reutilizado ou reinterpretado em outro formato, desde que o número de componentes e a contagem de bits de cada componente sejam os mesmos em ambos os formatos.

Um recurso único pode ser vinculado a vários estágios de pipeline, desde que cada um tenha um modo de exibição exclusivo que qualifique totalmente os formatos em cada local. Por exemplo, um recurso criado com o formato DXGI \_ \_ R32G32B32A32 sem \_ tipo pode ser usado como um formato dxgi \_ \_ R32G32B32A32 \_ float e um formato dxgi \_ \_ R32G32B32A32 \_ uint em locais diferentes no pipeline simultaneamente.

## <a name="resource-views"></a>Exibições de recursos

Os recursos podem ser armazenados em formatos de memória de uso geral para que possam ser compartilhados por vários estágios de pipeline. Um estágio de pipeline interpreta os dados de recursos usando uma exibição. Uma exibição de recurso é conceitualmente semelhante à conversão dos dados do recurso para que ele possa ser usado em um contexto específico.

Um modo de exibição pode ser usado com um recurso sem tipo. Ou seja, você pode criar um recurso em tempo de compilação e declarar o tipo de dados quando o recurso estiver associado ao pipeline. Uma exibição criada para um recurso de tipoless sempre tem o mesmo número de bits por componente; a maneira como os dados são interpretados depende do formato especificado. O formato especificado deve ser da mesma família que o formato não tipado usado ao criar o recurso. Por exemplo, um recurso criado com o \_ formato sem tipo R8G8B8A8 não pode ser exibido como um \_ recurso float R32, embora ambos os formatos possam ter o mesmo tamanho na memória.

Uma exibição também expõe outros recursos, como a capacidade de ler as superfícies de profundidade/estêncil em um sombreador, gerar um cubemap dinâmico em uma única passagem e renderizar simultaneamente para várias fatias de um volume.



| Interface de recurso                                             | Description                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Acesse um recurso de textura durante o teste de estêncil de profundidade.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Acesse um recurso de textura que é usado como um destino de renderização.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Acesse um recurso do sombreador, como um buffer constante, um buffer de textura, uma textura ou uma amostra. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Acessar um recurso não ordenado usando um sombreador de pixel ou um sombreador de computação.                        |



 

## <a name="raw-views-of-buffers"></a>Exibições brutas de buffers

Você pode considerar um buffer bruto, que também pode ser chamado de [buffer de endereço de byte](direct3d-11-advanced-stages-cs-resources.md), como um conjunto de bits para o qual você deseja acesso bruto, ou seja, um buffer que pode ser acessado por meio de partes de um para valores de endereço sem tipo de 4 32 bits. Você indica que deseja acesso bruto a um buffer (ou uma exibição bruta de um buffer) ao chamar um dos seguintes métodos para criar uma exibição para o buffer:

-   Para criar um modo de exibição de recurso de sombreador (SRV) para o buffer, chame [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) com o sinalizador [**D3D11 \_ BUFFEREX \_ SRV \_ Flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag). Você especifica esse sinalizador no membro **flags** da estrutura [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) . Você define **D3D11 \_ BUFFEREX \_ SRV** no membro **BUFFEREX** da estrutura [**desc da \_ \_ exibição de \_ recursos \_ do sombreador D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) para a qual o parâmetro *pDesc* dos pontos **ID3D11Device:: CreateShaderResourceView** . Você também define o valor de [**\_ \_ \_ BUFFEREX de dimensão SRV D3D11**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) no membro **ViewDimension** da **exibição de recursos do \_ sombreador D3D11 \_ \_ \_ desc** para indicar que o SRV é uma exibição bruta.
-   Para criar um UAV (modo de exibição de acesso não ordenado) para o buffer, chame [**ID3D11Device:: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) com o sinalizador [**D3D11 \_ buffer \_ UAV \_ Flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag). Você especifica esse sinalizador no membro **flags** da estrutura [**UAV do \_ buffer \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) . Você define **D3D11 \_ buffer \_ UAV** no membro de **buffer** da estrutura [**desc de \_ exibição de \_ acesso \_ \_ não ordenado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) para a qual o parâmetro *pDesc* de **ID3D11Device:: CreateUnorderedAccessView** pontos. Você também define o valor do [**\_ buffer de \_ dimensão \_ D3D11 UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) no membro **ViewDimension** de **D3D11 \_ modo de \_ exibição de acesso não ordenado \_ \_ desc** para indicar que UAV é uma exibição bruta.

Você pode usar os tipos de objeto HLSL [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) e [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) ao trabalhar com buffers brutos.

Para criar um modo de exibição bruto para um buffer, primeiro você deve chamar [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) com o sinalizador de [**\_ \_ \_ \_ permissão \_ \_ de buffer misc do D3D11 de recursos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para criar o recurso de buffer subjacente. Você especifica esse sinalizador no membro **MiscFlags** da estrutura [**Desc do \_ buffer \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para o qual o parâmetro *PDesc* dos pontos **ID3D11Device:: CreateBuffer** . Não é possível combinar o sinalizador de **D3D11 do \_ recurso de \_ buffer diverso \_ \_ permitir \_ \_ exibições brutas** com o [**\_ buffer variado do recurso D3D11 \_ \_ \_ estruturado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag). Além disso, se você especificar o [**\_ \_ \_ buffer constante de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) no **BindFlags** da **\_ \_ Desc do buffer D3D11**, não será possível especificar o **\_ buffer misc do recurso D3D11 \_ \_ \_ permitir \_ \_ exibições brutas** em **MiscFlags**. Isso não é uma limitação de apenas exibições brutas porque os buffers de constante já têm uma restrição de que eles não podem ser combinados com nenhuma outra exibição.

Além dos casos inválidos anteriores, quando você cria um buffer com o [**\_ buffer misc de recurso D3D11 \_ \_ \_ permite \_ \_ exibições brutas**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), você não está limitado em funcionalidade versus não configurar o **buffer de \_ recurso \_ variado D3D11 \_ \_ permitir \_ \_ exibições brutas**. Ou seja, você pode usar um buffer desse tipo para acesso não-bruto de várias maneiras possíveis com o Direct3D. Se você especificar o sinalizador de **permitir D3D11 de \_ \_ \_ buffer \_ \_ \_ variado do recurso** , você só aumentará a funcionalidade disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> <dt>

[Novos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 