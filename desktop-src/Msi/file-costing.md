---
description: O custo é o processo de determinação dos requisitos totais de espaço em disco para uma instalação.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Custo do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764659"
---
# <a name="file-costing"></a>Custo do arquivo

O custo é o processo de determinação dos requisitos totais de espaço em disco para uma instalação. Os elementos calculados no processo de custo de arquivo incluem a quantidade de espaço em disco em que os arquivos são instalados ou removidos, bem como a quantidade de espaço em disco ocupada por entradas de registro, atalhos e outros arquivos diversos. Os arquivos existentes agendados para serem substituídos também são calculados nos totais de custo do disco.

Os custos totais são acumulados em uma base por[componente](components-and-features.md) e consistem em três partes separadas: custos locais, custos de origem e custos de remoção. Essas partes correspondem ao custo do disco incorrido se o componente está instalado localmente, instalado para execução a partir da mídia de origem ou removido.

Todos os cálculos que envolvem o custo de instalação de arquivos dependem do volume de disco no qual o arquivo deve ser instalado ou removido. Cada vez que o diretório associado a um componente é alterado, os custos dos arquivos de instalação controlados por esse componente devem ser recalculados. Por exemplo, como uma alteração de diretório também pode implicar uma alteração de volume, os tamanhos de arquivo clusterizados devem ser recalculados. Além disso, o novo diretório deve ser verificado para determinar se os arquivos existentes que podem ser substituídos devem ser levados em conta.

Depois que a ação [CostInitialize](costinitialize-action.md) for chamada, a ação [filecost](filecost-action.md) deverá ser chamada. A ação CostInitialize inicializa as rotinas internas do instalador que calculam dinamicamente os custos de disco envolvidos nas ações de instalação padrão. Nenhum outro cálculo de custo dinâmico é feito neste momento.

Em seguida, a ação [CostFinalize](costfinalize-action.md) deve ser chamada. Esta ação finaliza todos os cálculos de custo e disponibiliza os dados de custos por meio da tabela de [componentes](component-table.md) .

Depois que a ação [CostFinalize](costfinalize-action.md) concluir a execução, a tabela de [componentes](component-table.md) será totalmente inicializada e uma sequência de caixa de diálogo da interface do usuário que contém um controle [SelectionTree](selectiontree-control.md) poderá ser iniciada se necessário. As caixas de diálogo da interface do usuário podem oferecer a opção de alterar o estado de seleção ou o diretório de destino de qualquer recurso na tabela de [recursos](feature-table.md) para o usuário. O processo é semelhante quando o estado de seleção de um componente é alterado; no entanto, nesse caso, o custo dinâmico do componente alterado somente é recalculado.

Depois que o usuário tiver concluído a seleção de recursos na interface do usuário, a ação [InstallValidate](installvalidate-action.md) deverá ser chamada. Essa ação verifica se todos os volumes aos quais o custo foi atribuído têm espaço suficiente para a instalação.

 

 



