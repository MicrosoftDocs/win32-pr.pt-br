---
description: Para exibir uma caixa de diálogo que lista os objetos de desempenho e os contadores definidos no computador, chame a função PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Contadores de navegação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63278e0a531ec882bad6e102c89f6db0e0946a0d2a0a14b8736e7ee3aef6a8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011404"
---
# <a name="browsing-counters"></a>Contadores de navegação

Para exibir uma caixa de diálogo que lista os objetos de desempenho e os contadores definidos no computador, chame a função [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) . A caixa de diálogo permite que o usuário navegue e selecione contadores de desempenho. Use a estrutura de [**configuração do PDH \_ Browse \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) para especificar a configuração da caixa de diálogo. Por exemplo, você pode configurar a caixa de diálogo para retornar uma seleção ou várias seleções.

Na entrada, o membro **szReturnPathBuffer** contém o objeto de desempenho e o contador padrão selecionados na caixa de diálogo. Na saída, o buffer contém o objeto de desempenho e o contador que o usuário selecionou. Você também pode usar o membro **pCallBack** para especificar uma função de retorno de chamada para processar os nomes de contadores retornados pela caixa de diálogo.

Observe que essa caixa de diálogo pode retornar \_ o diálogo PDH \_ cancelado se **bSingleCounterPerDialog** for **false** e o usuário clicar no botão fechar, de modo que seu tratamento de erros teria que considerar isso.

Para obter um exemplo que usa a função [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) , consulte [procurar contadores de desempenho](browsing-performance-counters.md).

Para recuperar uma lista de objetos de desempenho no computador, você também pode chamar a função [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) . Para recuperar uma lista de contadores e instâncias para um objeto de desempenho, chame a função [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) . Você também pode usar essas funções para identificar os objetos de desempenho e os contadores contidos em um arquivo de log. Chamadas repetidas para **PdhEnumObjectItems** retornará a mesma lista de contadores e instâncias até que você chame **PdhEnumObjects** para atualizar a lista de objetos de desempenho primeiro. Para obter um exemplo que enumera objetos e contadores, consulte [Enumerando objetos de processo](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Selecionando a fonte de dados

Você pode usar [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) em conjunto com [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para solicitar que o usuário selecione se a fonte de dados está em tempo real ou em um arquivo de log e, se for um arquivo de log, seu nome. Se você não quiser que a caixa de diálogo da fonte de dados seja exibida, você pode chamar **PdhSelectDataSource** para exibir apenas o catálogo do navegador de arquivos. Para fazer isso, especifique \_ o navegador de arquivos de sinalizadores de PDH \_ \_ \_ somente como o segundo parâmetro da chamada para **PdhSelectDataSource**.

 

 



