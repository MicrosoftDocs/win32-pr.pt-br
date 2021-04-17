---
description: Com a versão 2,0, os contadores de desempenho alteraram a arquitetura para simplificar o processo de fornecimento de dados do contador aos consumidores.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Fornecendo dados de contador usando a versão 2,0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754613"
---
# <a name="providing-counter-data-using-version-20"></a>Fornecendo dados de contador usando a versão 2,0

Os provedores de dados de desempenho modernos usam um manifesto para definir os dados do contador e usam as APIs do provedor do contador de desempenho para gerenciar dados no contexto do provedor. Provedores implementados usando um manifesto e APIs de provedor de contador de desempenho geralmente são chamados de **provedores v2**. O Windows dá suporte a provedores v2 de modo de usuário no Windows Vista ou em provedores v2 de modo kernel no Windows 7 ou posterior.

Esta página descreve os provedores v2 de modo de usuário. Para obter informações sobre provedores v2 de modo kernel, consulte [monitoramento de desempenho do modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

Em tempo de execução, os provedores v2 funcionam da seguinte maneira:

- O processo do provedor se registra no sistema do contador de desempenho do Windows chamando PerfStartProvider e PerfSetCounterSetInfo. O provedor, opcionalmente, fornece uma função de retorno de chamada que será notificada sobre solicitações do consumidor.
- O processo do provedor adiciona ou remove instâncias conforme apropriado usando PerfCreateInstance e PerfDeleteInstance. O provedor atualiza valores de contador quando eles mudam usando as APIs Perfset * * _.
- Um consumidor faz uma solicitação de dados de um CounterSet. O sistema verifica se o chamador tem permissões para coletar os dados. Em seguida, o sistema usa um thread de trabalho em execução no processo do provedor para lidar com a solicitação, invocando a função de retorno de chamada do provedor, se apropriado. O thread de trabalho copia os dados coletados em um buffer gerenciado pelo sistema, e o sistema retorna os dados para o consumidor.

## <a name="steps-to-creating-a-provider"></a>Etapas para criar um provedor

1. Escreva um manifesto que defina os dados do contador que seu provedor fornecerá. Para obter detalhes sobre como gravar o manifesto, consulte [esquema de contadores de desempenho](performance-counters-schema.md).
2. Use [ctrpp](ctrpp.md) para gerar o código de modelo que você inclui em seu provedor. O código do modelo inclui as estruturas que definem os conjuntos de contadores, as funções [_ *getinitialize* *](counterinitialize.md) e [**procleanup**](countercleanup.md) e as cadeias de caracteres de recurso.

   Seu provedor deve chamar as funções de [**reinicialização**](counterinitialize.md) e de [**contralimpeza**](countercleanup.md) . A **Metainicialização** chama a função [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) para registrar o provedor e também chama a função [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) para inicializar o conjunto de contadores. A **metalimpeza** chama a função [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para remover o registro do provedor.

3. Inclua o código de modelo da etapa anterior em seu projeto e conclua seu provedor.

   Para concluir o provedor, você precisa chamar a função [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) para cada instância do conjunto de contadores que você fornecer.

   Para definir os valores do contador, chame uma das seguintes funções:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   O benefício de usar o [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) é que você não precisa fazer uma chamada de função para definir ou atualizar o valor do contador, basta atualizar sua variável de contador local (a variável para a qual os pontos de referência) e os contadores de desempenho usam o ponteiro para acessar o valor do contador.

   Se você não usar [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), poderá usar as seguintes funções para incrementar ou decrementar o valor do contador:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Antes de o provedor sair, ele deve chamar o [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) para cada instância do conjunto de contadores que ele criou.

   Se você especificou o atributo de **retorno de chamada** no elemento [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) em seu manifesto ou usou o argumento **-NotificationCallback** ao chamar [ctrpp](ctrpp.md), deverá implementar a função de retorno de chamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) . Você passa a função de retorno de chamada para fazer a [**inicialização**](counterinitialize.md).

   Se você usou o **-MemoryRoutines** ao chamar [ctrpp](ctrpp.md), você deve implementar as funções de retorno de chamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) e [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Você passa as funções de retorno de chamada para fazer a [**inicialização**](counterinitialize.md).

4. Ao instalar seu provedor, use a ferramenta LodCtr para gravar o nome do arquivo binário que contém as cadeias de caracteres de recursos localizadas e as IDs de recurso no registro. Para obter detalhes sobre como usar LodCtr, consulte [esquema de contadores de desempenho](performance-counters-schema.md).

5. Ao desinstalar seu provedor, use a ferramenta UnlodCtr para remover as informações do provedor do registro.
