---
description: Recursos do Direct3D 10.1
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Recursos do Direct3D 10.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f674cc3ff5763fde77c13a3dac4a86a03d8bf8373bd5b34e9ffa74b21f563a47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371426"
---
# <a name="direct3d-101-features"></a>Recursos do Direct3D 10.1

O Direct3D 10.1 estende o conjunto de recursos do Direct3D 10.0 com os seguintes novos recursos:

-   Modos do Blend – modos de mesclagem independentes por destino de renderização usando a nova interface blend-state (consulte Interface [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). Operações de combinação de origem dupla são restritas para renderizar o slot de destino 0; você não pode gravar em outras saídas ou ter destinos de renderização vinculados a slots que não o slot 0.
-   Comportamento de rebaixamento – rostos de área zero são automaticamente eliminados; isso afeta apenas a renderização de wireframe.
-   Regras de ponto flutuante – usa as mesmas regras IEEE-754 para operações de ponto flutuante EXCEPT de 32 bits foram reforçadas para produzir um resultado dentro de 0,5 ULP (unidade último local) de 0,5 ULP do resultado infinitamente preciso. Isso se aplica à adição, subtração e multiplicação. (precisão para 0,5 ULP para multiplicação, 1,0 ULP para recíproco).
-   Formatos – a precisão da combinação float16 aumentou para 0,5 ULP. A combinação também é necessária para formatos UNORM16/SNORM16/SNORM8.
-   Suavização multisample – A multisampling foi aprimorada para generalizar a transparência baseada em cobertura e fazer com que o multiampling funcione com mais eficiência com a renderização de várias passões. Para fazer isso, todas as semânticas multisample são definidas como se o sombreador de pixel sempre fosse executado uma vez por exemplo (frequência de exemplo), calculando uma cor separada por amostra. Se um sombreador de pixel não usar nenhum atributos por exemplo, ele calculará o mesmo valor para cada amostra coberta em um pixel. Nesse caso, é equivalente ao hardware que executa o sombreador uma vez por pixel (frequência de pixel), replicando o resultado para todos os exemplos cobertos. Naturalmente, a execução em frequência de pixel sempre produz os mesmos resultados que executar o mesmo sombreador na frequência de exemplo, quando os atributos são amostrados em uma frequência de pixel. A estatística de pipeline PSInvocations é incrementada na frequência de exemplo, a menos que o sombreador esteja em execução na frequência de pixel.
-   Largura de banda do estágio do pipeline – aumento da quantidade de dados que podem ser passados entre os estágios do sombreador: 

    | Recurso                        | Limites                    |
    |---------------------------------|---------------------------|
    | Registros entre estágios do sombreador | 32 (componente de 32 bits x 4) |
    | Registros de entrada do sombreador de vértice   | 32                        |
    | Slots de entrada do Assembler de Entrada     | 32                        |

    

     

-   Regras de rasterização – as regras de rasterização foram alteradas para linhas, além disso, novas funcionalidades foram adicionadas.
    -   MultisampleEnable afeta apenas a rasterização de linha (pontos e triângulos não são afetados) e é usado para escolher um algoritmo de desenho de linha. Isso significa que não há mais suporte para alguns rasterização multisample do Direct3D 10.
    -   Nova execução do sombreador de pixel de frequência de exemplo com rasterização primitiva.
-   Recursos – CopyResource está habilitado em dois novos cenários:
    -   As superfícies MSAA de cor e profundidade/estêncil agora podem ser usadas com CopyResource como uma origem ou destino
    -   Conversão de formato durante a cópia entre determinados recursos pré-estruturados de 34/64/128 bits, recursos digitados e representações compactadas das mesmas larguras de bits.
-   Amostragem de textura – as instruções c e c lz de exemplo são definidas para funcionar com \_ \_ Texture2DArrays e TextureCubeArrays, usar o membro Location (o componente alfa) para especificar um índice de \_ matriz.
-   Exibições – TextureCube e a nova TextureCubeArray (consulte [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) não são recursos reais, mas são novas exibições em um recurso Texture2DArray. Crie uma exibição de recurso de um recurso Texture2DArray com um novo sinalizador de uso (D3D10 \_ RESOURCE \_ MISC TEXTURECUBE), use a nova interface \_ [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) para vincular uma exibição de textura de cubo ao pipeline.

Os novos recursos exigem um tipo de dispositivo 10.1 (consulte [**Interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) que pode ser criado chamando [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)ou você pode criar o dispositivo e trocar a cadeia ao mesmo tempo chamando [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1).

No Windows Vista Service Pack 1, as DLLs direct3D 10.0 e Direct3D 10.1 existem lado a lado no sistema. Para acessar os recursos do 10.1, faça o seguinte:

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Acessando recursos do 10.1 no Vista Gold e no Vista Service Pack 1

Os desenvolvedores que desejam dar suporte ao Vista Gold, bem como ao SP1, terão que levar em conta a falta das novas extensões de API 10.1 no Vista Gold. DXUT e D3DX10 fornecerão funções de conveniência para criar o dispositivo apropriado, com base nas DLLs disponíveis no sistema e no hardware disponível (10.0 ou 10.1). O dispositivo 10.1 herda do dispositivo 10.0 e pode ser recuperado usando QueryInterface(). É recomendável que cada aplicativo controle o tipo de dispositivo e mantenha um ponteiro para o dispositivo 10.1 (se disponível) para evitar chamadas frequentes de QueryInterface quando a funcionalidade 10.1 for desejada. Da mesma forma, em que 10.1 exibições de recursos e objetos de estado são associados pela classe personalizada de um aplicativo, é recomendável que o aplicativo acompanhe se o objeto é um tipo 10.0 ou 10.1 para evitar chamadas Redundantes queryInterface(). D3DX10 inclui um conjunto de funções de utilitário para simplificar esse processo (consulte [**D3DX10CreateDevice**](d3dx10createdevice.md) e [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Acessando recursos 10.1 no Vista Service Pack 1 exclusivamente

Alguns desenvolvedores podem optar por exigir o Vista Service Pack 1, que será distribuído amplamente para os usuários finais e inclui uma série de melhorias fora do Direct3D 10.1. Esses desenvolvedores podem usar exclusivamente os bibliotecas e os headers do Direct3D 10.1, utilizando uma dependência das DLLs do Direct3D 10.1 que suportam hardware 10.0 e 10.1 (algumas chamadas podem falhar, no entanto, em dispositivos 10.0 em que não há suporte para a nova funcionalidade).

Algumas observações adicionais:

-   As APIs expostas no D3DX10.dll aceitarão os dispositivos 10.0 e 10.1 e aproveitarão a funcionalidade 10.1 quando disponíveis.
-   D3D10SDKLayers.dll dá suporte a um dispositivo 10.1 e pode saída do spew de depuração apropriado para recursos 10.1.
-   D3D10Ref.dll implementa um dispositivo de software 10.0 e 10.1.
-   O D3DX10 e o FXC são suportados pelo modelo de sombreador 10.1 atualizado com os seguintes destinos: \_ vs. \_ 4 1, gs \_ 4 1, ps 4 1 e fx 4 1, que podem ser vinculados a um dispositivo \_ \_ \_ \_ \_ 10.1. Um dispositivo 10.1 dá suporte a sombreadores do modelo de sombreador 4.0 e 4.1.
-   A estrutura de efeito Direct3D 10.0 dá suporte a dispositivos 10.0 e 10.1, no entanto, qualquer técnica que inclua sombreadores do modelo de sombreador 4.1 ou os novos recursos 10.1 devem usar um dispositivo 10.1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



