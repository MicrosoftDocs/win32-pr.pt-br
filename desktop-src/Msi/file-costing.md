---
description: O custo é o processo de determinar o total de requisitos de espaço em disco para uma instalação.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Custo do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad2dc3ad9da4fab21345e74f3f9db99992445d7cf1e2266806bda55cd6ca638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529576"
---
# <a name="file-costing"></a>Custo do arquivo

O custo é o processo de determinar o total de requisitos de espaço em disco para uma instalação. Os elementos calculados no processo de custo de arquivo incluem a quantidade de espaço em disco no qual os arquivos são instalados ou removidos, bem como a quantidade de espaço em disco tomada por entradas do Registro, atalhos e outros arquivos diversos. Os arquivos existentes agendados para serem substituídos também são calculados nos totais de custo do disco.

Os custos totais são[](components-and-features.md) acumulados por componente e consistem em três partes separadas: custos locais, custos de origem e custos de remoção. Essas partes correspondem ao custo do disco incorrido se o componente estiver instalado localmente, instalado para ser executado da mídia de origem ou removido.

Todos os cálculos que envolvem o custo de instalação de arquivos dependem do volume de disco no qual o arquivo deve ser instalado ou removido. Cada vez que o diretório associado a um componente é atualizado, os custos dos arquivos de instalação controlados por esse componente devem ser recalculados. Por exemplo, como uma alteração de diretório também pode implicar uma alteração de volume, os tamanhos de arquivos clusterados devem ser recalculados. Além disso, o novo diretório deve ser verificado para determinar se todos os arquivos existentes que podem ser substituídos devem ser levados em conta.

Depois que [a ação CostInitialize](costinitialize-action.md) for chamada, a [ação FileCost](filecost-action.md) deverá ser chamada. A ação CostInitialize inicializa as rotinas internas do instalador que calculam dinamicamente os custos de disco envolvidos com as ações de instalação padrão. Nenhum outro cálculo de custo dinâmico é feito neste momento.

Em seguida, [a ação CostFinalize](costfinalize-action.md) deve ser chamada. Essa ação finaliza todos os cálculos de custo e disponibiliza os dados de custo por meio da [tabela Componente.](component-table.md)

Depois que a [ação CostFinalize](costfinalize-action.md) concluir a execução, a tabela Componente será totalmente inicializada e uma sequência de caixa de diálogo da interface do usuário que contém um controle [SelectionTree](selectiontree-control.md) poderá ser iniciada, se necessário. [](component-table.md) As caixas de diálogo da interface do usuário podem oferecer a opção de alterar o estado de seleção ou o diretório de destino de qualquer recurso na [tabela](feature-table.md) Recurso para o usuário. O processo é semelhante quando o estado de seleção de um componente muda; no entanto, nesse caso, o custo dinâmico do componente alterado é recalculado.

Depois que o usuário concluir a seleção de recursos na interface do usuário, [a ação InstallValidate](installvalidate-action.md) deverá ser chamada. Essa ação verifica se todos os volumes aos quais o custo foi atribuído têm espaço suficiente para a instalação.

 

 



