---
title: APIs de recursos de lado
description: As APIs descritas nesta seção funcionam com os recursos de lado e o pool de blocos.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0d97f5272f4f96db56e6e89b871951de035105
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363722"
---
# <a name="tiled-resource-apis"></a>APIs de recursos de lado

As APIs descritas nesta seção funcionam com os recursos de lado e o pool de blocos.

-   [Atribuindo blocos de um pool de peças a um recurso](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Consultando suporte e disposição do recurso](#querying-resource-tiling-and-support)
-   [Copiando dados em ladrilhos](#copying-tiled-data)
-   [Redimensionando o pool de blocos](#resizing-tile-pool)
-   [Barreira de recurso por lado](#tiled-resource-barrier)
-   [Tópicos relacionados](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Atribuindo blocos de um pool de peças a um recurso

As APIs [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) manipulam e consultam mapeamentos de bloco. As chamadas de atualização afetam apenas os blocos identificados na chamada, e outros são deixados conforme definido anteriormente.

Qualquer bloco específico de um pool de peças pode ser mapeado para vários locais em um recurso e até mesmo vários recursos. Esse mapeamento inclui blocos em um recurso que têm um layout escolhido pela implementação ([empacotamento de mipmap](mipmap-packing.md)), em que vários mipmaps são empacotados juntos em um único bloco. O problema é que, se os dados forem gravados no bloco por meio de um mapeamento, mas lidos por meio de um mapeamento configurado de forma diferente, os resultados serão indefinidos. No entanto, o uso cuidadoso dessa flexibilidade ainda pode ser útil para um aplicativo, como compartilhar um bloco entre os recursos que não serão usados simultaneamente, onde o conteúdo do bloco sempre será inicializado por meio do mesmo mapeamento de recursos, pois eles serão lidos posteriormente. Da mesma forma, um bloco mapeado para manter o mipmaps empacotado de vários recursos diferentes com as mesmas dimensões de superfície funcionará bem. os dados serão exibidos da mesma forma em ambos os mapeamentos.

Alterações nas atribuições de bloco para um recurso podem ser feitas a qualquer momento em um contexto imediato ou adiado.

## <a name="querying-resource-tiling-and-support"></a>Consultando suporte e disposição do recurso

Para consultar o recurso em blocos, use [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling).

Para outro suporte ao lado do recurso, use [**ID3D11Device2:: CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copiando dados em ladrilhos

Quaisquer métodos no Direct3D para mover dados em todo o trabalho com recursos de lado, assim como se eles não fossem lado, exceto que as gravações em áreas não mapeadas são descartadas e as leituras de áreas não mapeadas produzem 0. Se uma operação de cópia envolver a gravação no mesmo local de memória várias vezes porque vários locais no recurso de destino são mapeados para a mesma memória de bloco, as gravações resultantes em blocos de vários mapeados são não determinísticas e não repetíveis. Ou seja, os acessos acontecem em qualquer ordem em que o hardware for executar a cópia.

O Direct3D 11,2 apresenta métodos para essas maneiras adicionais de copiar:

-   Copiar entre blocos em um recurso do lado do ladrilho (com granularidade de bloco de 64 KB) e (de/para) um buffer na memória da GPU (unidade de processamento gráfico) (ou recurso de preparo)- [ **ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copiar da memória fornecida pelo aplicativo para blocos em um recurso de lado-a- [ **ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Esses métodos swizzle/deswizzle conforme necessário e permitem um bloco de \_ D3D11 \_ copiar \_ sem \_ sinalizador de substituição quando o chamador promete que a memória de destino não é referenciada pelo trabalho de GPU que está em trânsito.

Os blocos envolvidos na cópia não podem incluir blocos que contenham mipmaps empacotados ou que tenham resultados indefinidos. Para transferir dados de/para o mipmaps que os pacotes de hardware em um único bloco, você deve usar as APIs de cópia/atualização padrão (não específicas do bloco) ou [**ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) para toda a cadeia MIP.

**Observação em [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** usar [**ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) em um recurso com blocos parcialmente mapeados produzirá resultados que simplesmente seguem as regras para leitura e gravação de **NULL** aplicadas a qualquer algoritmo que o hardware e o driver de vídeo aconteçam para serem usados para **GenerateMips**. Portanto, não é particularmente útil que um aplicativo se preocupe em fazer isso, a menos que as áreas com mapeamentos **nulos** (e seus efeitos em outros MIPS durante a fase de geração) não tenham nenhuma conseqüência sobre as partes da superfície para as quais o aplicativo se preocupa.

Copiar dados de bloco de uma superfície de preparo ou da memória do aplicativo seria a maneira de carregar blocos que podem ter sido transmitidos em disco, por exemplo. Uma variação na transmissão fora do disco é carregar algum tipo de dados compactados para a memória da GPU e, em seguida, decodificar na GPU. O destino de decodificação pode ser um recurso de buffer na memória de GPU, do qual o [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) , em seguida, copia para o recurso em ladrilhos real. Essa etapa de cópia permite que a GPU swizzle quando o padrão de swizzle não é conhecido. Swizzling não será necessário se o próprio recurso de ladrilho for um recurso de buffer (por exemplo, em oposição a uma textura).

O layout de memória dos blocos no lado do recurso de buffer que não se dispõe de lado da cópia é simplesmente linear na memória dentro dos blocos de 64 KB, que o hardware e o driver de vídeo swizzle/deswizzle por bloco, conforme apropriado, ao transferir de/para um recurso de lado. Para superfícies de MSAA (multiamostragem), as amostras de cada pixel são percorridas em ordem de índice de exemplo antes de passar para o próximo pixel. Para blocos parcialmente preenchidos no lado direito (para uma superfície que tenha uma largura que não seja um múltiplo de largura de bloco em pixels), a densidade/distância para mover uma linha é o tamanho total em bytes do número de pixels que se ajustaria ao bloco se o bloco estivesse cheio. Portanto, pode haver uma lacuna entre cada linha de pixels na memória. Para simplificar a especificação, mipmaps menor do que um bloco não é empacotado juntos no layout linear. Isso parece ser um desperdício de espaço de memória, mas, conforme mencionado, copie para MIPS que os pacotes de hardware juntos não são permitidos por meio de [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) ou [**UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles). O aplicativo só pode usar as \* APIs UpdateSubresource () ou CopySubresource \* () genéricas para copiar pequenas MIPS individualmente, embora no caso de CopySubresource \* (), que significa que a memória linear deve ser a mesma dimensão que o recurso de lado-a-CopySubresource \* () não pode copiar de um recurso de buffer para um Texture2D para a instância.

Se um swizzle de hardware padrão for definido, os sinalizadores poderão ser adicionados para indicar que os dados no buffer devem ser interpretados nesse formato (nenhum swizzle necessário na transferência), embora abordagens alternativas para carregar dados também possam fazer sentido nesse caso, como permitir que os aplicativos acessem diretamente a memória do pool de blocos.

Operações de cópia podem ser feitas em um contexto imediato ou adiado.

## <a name="resizing-tile-pool"></a>Redimensionando o pool de blocos

Para redimensionar um pool de blocos, use [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barreira de recurso por lado

Para especificar uma restrição de ordenação de acesso a dados entre vários recursos de lado, use [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos em ladrilho](tiled-resources.md)
</dt> </dl>

 

 




