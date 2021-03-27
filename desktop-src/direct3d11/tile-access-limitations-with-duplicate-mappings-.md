---
title: Limitações de acesso de bloco com mapeamentos duplicados
description: Esta seção descreve as limitações de acesso de bloco com mapeamentos duplicados.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005040"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Limitações de acesso de bloco com mapeamentos duplicados

Esta seção descreve as limitações de acesso de bloco com mapeamentos duplicados.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copiando recursos em ladrilho com sobreposição de origem e destino

Se os blocos na área de origem e de destino de uma operação de cópia \* tiverem mapeamentos duplicados na área de cópia que teriam sobreposição, mesmo se os dois recursos não fossem recursos de lado, e a operação de cópia \* der suporte a cópias sobrepostas, a operação de cópia \* se comportará bem (como se a origem fosse copiada para um local temporário antes de ir para o Mas, se a sobreposição não for óbvia (por exemplo, os recursos de origem e destino são diferentes, mas compartilham mapeamentos, ou os mapeamentos são duplicados sobre uma determinada superfície), os resultados da operação de cópia nos blocos que são compartilhados serão indefinidos.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copiando para o recurso de bloco com blocos duplicados na área de destino

A cópia para um recurso de bloco ao lado com blocos duplicados na área de destino produz resultados indefinidos nesses blocos, a menos que os próprios dados sejam idênticos; blocos diferentes podem gravar os blocos em ordens diferentes.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>Acessos UAV a mapeamentos de blocos duplicados

Suponha que um modo de exibição de acesso não ordenado (UAV) em um recurso de mosaico tenha mapeamentos de bloco duplicados em sua área ou com outros recursos associados ao pipeline. A ordenação dos acessos a estes blocos duplicados é indefinida se realizada por threads diferentes, assim como qualquer ordenação de acesso da memória a UAVs em geral é não ordenada.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Renderizando após alterações no mapeamento de blocos ou atualizações de conteúdo de mapeamentos externos

Se os mapeamentos de bloco de um recurso do lado do ladrilho tiverem sido alterados ou se o conteúdo em blocos de pool de mosaico mapeados tiver mudado por meio de mapeamentos de outro recurso, e o recurso de bloco ao lado será renderizado por meio da exibição de destino de renderização ou exibição de estêncil de profundidade, o aplicativo deverá limpar (usando as APIs de limpeza de função fixa) ou copiar totalmente usando \* APIs Copy/update \* os blocos que foram alterados dentro da área que está sendo renderizada (mapeada ou não). A falha de um aplicativo para limpar ou copiar nesses casos faz com que estruturas de otimização de hardware para a exibição de destino de renderização determinada ou exibição de estêncil de profundidade sejam obsoletas e resultarão em resultados de renderização de lixo em algum hardware e inconsistência em diferentes hardwares. Essas estruturas de dados de otimização ocultas usadas pelo hardware podem ser mapeamentos locais a individuais e não visíveis para outros mapeamentos na mesma memória.

A operação [**ID3D11DeviceContext1:: Clearview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) dá suporte à limpeza de exibições de destino de renderização com retângulos. Para hardware que dá suporte a recursos de lado, o **Clearview** também deve oferecer suporte à limpeza de exibições de estêncil de profundidade com retângulos, apenas para superfícies de profundidade (sem estêncil). Essa operação permite que os aplicativos limpem apenas a área necessária de uma superfície.

Se um aplicativo precisar preservar o conteúdo de memória existente de áreas em um recurso de lado-a-ponto em que os mapeamentos foram alterados, esse aplicativo deverá solucionar o requisito claro. O aplicativo pode realizar essa solução alternativa salvando primeiro o conteúdo em que os mapeamentos de bloco foram alterados (copiando-os para uma superfície temporária, por exemplo, usando [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)), emitindo o comando clear necessário e, em seguida, copiando o conteúdo de volta. Embora isso conclua a tarefa de preservar o conteúdo da superfície para renderização incremental, a desvantagem é que o desempenho da renderização subsequente na superfície poderá ser prejudicado porque as otimizações de renderização poderão ser perdidas.

Se um bloco for mapeado em vários recursos de lado, ao mesmo tempo e os conteúdos de bloco forem manipulados por qualquer meio (renderizar, copiar e assim por diante) por meio de um dos recursos ao lado do xadrez, se o mesmo bloco for renderizado por meio de qualquer outro recurso de lado, o bloco deverá ser limpo primeiro conforme descrito anteriormente.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Renderizando blocos compartilhados fora da área de renderização

Suponha que uma área em um recurso do lado do xadrez esteja sendo renderizada e os blocos do pool de blocos referenciados pela área de renderização também sejam mapeados para fora da área de renderização (incluindo por meio de outros recursos de lado, ao mesmo tempo ou não). Não há garantira de que os dados renderizados nesses blocos aparecerão corretamente quando visualizados por meio de outros mapeamentos, mesmo que o layout de memória subjacente seja compatível. Isso se deve às estruturas de dados de otimização que alguns hardwares usam que podem ser mapeamentos locais a individuais para superfícies renderizáveis e não visíveis para outros mapeamentos no mesmo local de memória. Você pode usar uma solução alternativa para essa restrição copiando do mapeamento renderizado para todos os outros mapeamentos na mesma memória que pode ser acessada (ou limpando essa memória ou copiando outros dados para ela se o conteúdo antigo não for mais necessário). Embora essa solução alternativa pareça redundante, isso faz com que todos os outros mapeamentos para a mesma memória entendam corretamente como acessar seu conteúdo, e pelo menos a economia de memória de se ter apenas uma única memória física de backup permanece intacta. Além disso, quando você alterna entre o uso de diferentes recursos de lado do toque que compartilham mapeamentos (a menos que apenas leitura), você deve chamar a API [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) entre as opções.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Renderizando blocos compartilhados dentro da área de renderização

Se uma área em um recurso de bloco ao lado estiver sendo renderizada para e dentro da área de renderização, vários blocos serão mapeados para o mesmo local do pool de blocos, os resultados de renderização serão indefinidos nesses blocos.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilidade de dados entre blocos de compartilhamento de recursos

Suponha que vários recursos ao lado dos blocos tenham mapeamentos para os mesmos locais de pool de peças e cada recurso é usado para acessar os mesmos dados. Esse cenário só será válido se as outras regras sobre como evitar problemas com estruturas de otimização de hardware forem evitadas, as chamadas apropriadas para [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) são feitas, e os recursos do lado do ladrilho são compatíveis entre si. O último é descrito aqui em termos de o que significa que os blocos de compartilhamento de recursos ao lado do bloco são incompatíveis. As condições de incompatibilidade de acesso aos mesmos dados em mapeamentos de blocos duplicados são o uso de diferentes dimensões ou formatos de superfície, ou diferenças na presença de sinalizadores de associação do destino de renderização ou do estêncil de profundidade nos recursos. A gravação na memória com um tipo de mapeamento gera resultados indefinidos quando, subsequentemente, você lê ou renderiza usando um mapeamento de um recurso incompatível. Se os outros mapeamentos de compartilhamento de recursos forem inicializados primeiro com novos dados (reciclando a memória para um objetivo diferente), a operação de leitura ou renderização subsequente funcionará bem, pois não haverá sangria dos dados entre interpretações incompatíveis. Mas, você deve chamar a API **TiledResourceBarrier** quando alternar entre o acesso a mapeamentos incompatíveis como este.

Se o sinalizador de associação do destino de renderização ou do estêncil de profundidade não estiver definido em qualquer um dos recursos que compartilham mapeamentos entre si, haverá bem menos restrições. Contanto que os tipos de formato e superfície (por exemplo, Texture2D) sejam os mesmos, os blocos poderão ser compartilhados. Formatos diferentes compatíveis são casos como superfícies de BC \* e o tamanho equivalente, sem compactação de 32 bits ou 16 bits por formato de componente, como BC6H e R32G32B32A32. Muitos formatos de 32 bits por elemento também podem ter um alias com R32 \_ \* (R10G10B10A2 \_ \* , R8G8B8A8 \_ \* , B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16 \_ \* ); essa operação sempre foi permitida para recursos que não são de lado do ladrilho.

Não há problema no compartilhamento entre blocos compactados e não compactados quando os formatos são compatíveis e os blocos são preenchidos com cor sólida.

Por fim, se não houver nada em comum nos mapeamentos de blocos de compartilham recursos, exceto que nenhum apresente sinalizadores de associação do destino de renderização ou do estêncil de profundidade, somente a memória preenchida com 0 poderá ser compartilhada com segurança; o mapeamento aparecerá como o valor que o 0 decodificar para a definição do formato de recurso específico (normalmente 0).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




