---
title: Mapeamentos estão em um pool de blocos
description: Quando um recurso é criado com o \_ sinalizador de \_ lado diverso do recurso D3D11 \_ , os blocos que compõem o recurso são apontados em locais em um pool de peças.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a31d2e8cd4457281c047db514dd2450d3bf70d85be7e4933cb7e5f5e026a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045614"
---
# <a name="mappings-are-into-a-tile-pool"></a>Mapeamentos estão em um pool de blocos

Quando um recurso é criado com o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , os blocos que compõem o recurso são apontados em locais em um pool de peças. Um pool de blocos é um pool de memória (sustentado por uma ou mais alocações nos bastidores - nunca vistos pelo app). O sistema operacional e o driver de vídeo gerenciam esse pool de memória, e o volume da memória é entendido facilmente por um app. Os recursos de blocos gráficos mapeiam as regiões de 64 KB apontando para locais em um pool de peças. Um resultado dessa configuração é permitir que vários recursos compartilhem e reutilizem os mesmos blocos, e também que os mesmos blocos sejam reutilizados em locais diferentes em um recurso, se desejado.

O custo da flexibilidade de preenchimento dos blocos de um recurso de um pool de blocos é que ele precisa definir e manter o mapeamento dos blocos no pool que representam aqueles necessários para o recurso. Os mapeamentos de blocos podem ser alterados. Além disso, nem todos os blocos em um recurso precisam ser mapeadas simultaneamente; um recurso pode ter mapeamentos **NULOS**. Um mapeamento **NULO** define um bloco como não disponível do ponto de vista do recurso que o acessa.

Vários pools de blocos podem ser criados, e qualquer número de recursos de blocos pode ser mapeado para um determinado pool de peças ao mesmo tempo. Os pools de bloco também podem ser aumentados ou reduzidos. Para obter mais informações, consulte [Redimensionamento do pool de blocos](tile-pool-resizing.md). Uma restrição que existe para simplificar a implementação do driver de vídeo e do tempo de execução é que um determinado recurso de mosaico só pode ter mapeamentos em no máximo um pool de peças por vez (em vez de ter mapeamento simultâneo para vários pools de blocos).

A quantidade de armazenamento que está associada a um recurso de mosaico (ou seja, memória de pool de blocos independente) é basicamente proporcional ao número de blocos realmente mapeados para o pool em um determinado momento. No hardware, esse fato se resume ao dimensionamento do volume de memória para armazenamento da tabela de página aproximadamente com a quantidade de blocos mapeados (por exemplo, usando um esquema de tabela de vários níveis de página conforme apropriado).

O pool de blocos pode ser pensado como uma abstração de software que permite aos apps Direct3D estarem efetivamente prontos para programar as tabelas de página na unidade de processamento gráfico (GPU) sem precisar saber os detalhes de implementação de nível baixo (ou processar endereços de ponteiro diretamente). Os pools de blocos não se aplicam a quaisquer níveis adicionais de indireção no hardware. As otimizações de uma única tabela de página de nível único usando construções como diretórios de página são independentes do conceito de pool de blocos.

Vamos explorar qual armazenamento a tabela de página pode exigir na pior das hipóteses (embora na prática as implementações exigem apenas armazenamento aproximadamente proporcional ao que é mapeado).

Considere que cada entrada da tabela de página é de 64 bits.

Para o pior caso, o tamanho da tabela de página de paginação é atingido para uma única superfície, dado os limites de recursos no Direct3D 11, suponha que um recurso de mosaico seja criado com um formato de 128 bits por elemento (por exemplo, um float de RGBA), para que um bloco de 64 KB contenha apenas 4096 pixels. O tamanho máximo de [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com suporte de 16384 \* 16384 \* 2048 (mas com apenas um único mipmap) EXIGIRIA cerca de 1 GB de armazenamento na tabela de página, se totalmente populado (não incluindo mipmaps) usando entradas da tabela de bits 64. A adição de mipmaps implica no crescimento do armazenamento de tabela de página totalmente mapeada (pior hipótese) em aproximadamente um terço, cerca de 1,3 GB.

Nesse caso, seria equivalente a fornecer acesso a aproximadamente 10,6 terabytes de memória endereçável. Pode haver um limite na quantidade de memória endereçável. Porém, isso reduziria esses valores, talvez próximos do intervalo de terabytes.

Outro caso a ser levado em consideração é um único recurso de lado do [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) de 16384 \* 16384 com um formato com 32 bits por elemento, incluindo mipmaps. O espaço necessário em uma tabela de página totalmente preenchida é de aproximadamente 170 KB com entradas de tabela de 64 bits.

Por fim, considere um exemplo usando um formato BC, diga BC7 com 128 bits por bloco de 4 x 4 pixels. Isso equivale a um byte por pixel. Um [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) de 16384 \* 16384 \* 2048, incluindo MIPMAPS exigiria aproximadamente 85MB para popular completamente essa memória em uma tabela de página. Isso não é errado, Considerando que isso permite que um recurso de lado-a-intervalo abranja 550 gigapixels (512 GB de memória nesse caso).

Na prática, essa quantidade de mapeamentos totais não seria definido considerando que a quantidade de memória física disponível não permite que essa quantidade seja mapeada e referenciada ao mesmo tempo. No entanto, com um pool de blocos, os apps podem optar por reutilizar blocos (um exemplo simples, reutilizar um bloco colorido "preto" para grandes regiões de preto em uma imagem), usando efetivamente o pool de blocos (ou seja, os mapeamentos de tabela de página) como uma ferramenta de compactação de memória.

O conteúdo inicial da tabela da página é **NULO** para todas as entradas. Os apps também não podem passar dados iniciais do conteúdo da memória da superfície, pois já começa sem suporte da memória.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criação de pool de blocos](tile-pool-creation.md)<br/>                                                 | Um pool de blocos é criado por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando o sinalizador de [**\_ \_ \_ \_ pool de blocos diversos do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) no membro **MiscFlags** da estrutura [**\_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para a qual o parâmetro *pDesc* aponta. <br/> |
| [Redimensionamento de pool de blocos](tile-pool-resizing.md)<br/>                                                 | Use a API [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) para aumentar um pool de blocos se o aplicativo precisar de mais um conjunto de trabalho para o mapeamento de recursos lado-a-quadro ou para reduzir se for necessário menos espaço. <br/>                                                                                                                    |
| [Controle de risco versus recursos de pool de blocos](hazard-tracking-versus-tile-pool-resources.md)<br/> | Para recursos sem blocos gráficos, o Direct3D pode impedir determinadas condições de risco durante a renderização, mas como o controle de riscos seria em um nível de bloco para recursos lado-a-quadrado, controlar condições de risco durante o processamento de recursos ao lado pode ser muito caro. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

