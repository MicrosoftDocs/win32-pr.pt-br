---
description: Com a versão 2.0, os Contadores de Desempenho mudaram a arquitetura para simplificar o processo de fornecimento de dados de contador aos consumidores.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Fornecendo dados de contador usando a versão 2.0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8e839fb72f8cbd8272f9afd89aa3456e1e0b08fc7197dd992b1069fec7ce108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143789"
---
# <a name="providing-counter-data-using-version-20"></a>Fornecendo dados de contador usando a versão 2.0

Provedores de dados de desempenho modernos usam um manifesto para definir os dados do contador e usar APIs do provedor do contador de desempenho para gerenciar dados dentro do contexto do provedor. Provedores implementados usando um provedor de contador de desempenho e manifesto geralmente são chamados **de provedores V2.** Windows dá suporte a provedores de modo de usuário V2 no Windows Vista ou em provedores de modo kernel V2 posteriores Windows 7 ou posterior.

Esta página descreve os provedores de modo de usuário V2. Para obter informações sobre provedores de modo kernel V2, consulte [Monitoramento de desempenho do modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

Em runtime, os provedores V2 funcionam da seguinte forma:

- O processo do provedor registra-se com o sistema Windows contadores de desempenho chamando PerfStartProvider e PerfSetCounterSetInfo. Opcionalmente, o provedor fornece uma função de retorno de chamada que será notificada sobre solicitações do consumidor.
- O processo do provedor adiciona ou remove instâncias conforme apropriado usando PerfCreateInstance e PerfDeleteInstance. O provedor atualiza os valores do contador quando eles mudam usando APIs PerfSet***.
- Um consumidor faz uma solicitação de dados de um contador. O sistema verifica se o chamador tem permissões para coletar os dados. Em seguida, o sistema usa um thread de trabalho em execução no processo do provedor para manipular a solicitação, invocando a função de retorno de chamada do provedor, se apropriado. O thread de trabalho copia os dados coletados em um buffer gerenciado pelo sistema e, em seguida, o sistema retorna os dados para o consumidor.

## <a name="steps-to-creating-a-provider"></a>Etapas para criar um provedor

1. Escreva um manifesto que define os dados do contador que seu provedor fornecerá. Para obter detalhes sobre como escrever o manifesto, consulte [Esquema de contadores de desempenho](performance-counters-schema.md).
2. Use [CTRPP](ctrpp.md) para gerar o código de modelo que você inclui em seu provedor. O código do modelo inclui as estruturas que definem os conjuntos de contadores, as funções [**CounterInitialize**](counterinitialize.md) e [**CounterCleanup**](countercleanup.md) e as cadeias de caracteres de recurso.

   Seu provedor deve chamar as [**funções CounterInitialize**](counterinitialize.md) e [**CounterCleanup.**](countercleanup.md) **CounterInitialize** chama a [**função PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) para registrar o provedor e também chama a [**função PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) para inicializar o conjunto de contadores. O **CounterCleanup** chama a [**função PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para remover o registro do provedor.

3. Inclua o código do modelo da etapa anterior em seu projeto e conclua o provedor.

   Para concluir o provedor, você precisa chamar a [**função PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) para cada instância do conjunto de contadores que você fornece.

   Para definir os valores do contador, chame uma das seguintes funções:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   O benefício de usar [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) é que você não precisa fazer uma chamada de função para definir ou atualizar o valor do contador, basta atualizar a variável de contador local (a variável para a qual os pontos de referência) e contadores de desempenho usam o ponteiro para acessar o valor do contador.

   Se você não usar [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), poderá usar as seguintes funções para incrementar ou decrementar o valor do contador:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Antes de o provedor sair, ele deve chamar [**PerfDeleteInstance para**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) cada instância do conjunto de contadores que ele criou.

   Se você especificou o atributo [](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) **de retorno** de chamada no elemento do provedor em seu manifesto ou usou o argumento **-NotificationCallback** ao chamar [CTRPP](ctrpp.md), deverá implementar a função de retorno de chamada [*ControlCallback.*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) Você passa a função de retorno de chamada [**para CounterInitialize**](counterinitialize.md).

   Se você usou **-MemoryRoutines** ao chamar [CTRPP,](ctrpp.md)deverá implementar as funções de retorno de chamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) e [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Você passa as funções de retorno de chamada [**para CounterInitialize**](counterinitialize.md).

4. Ao instalar o provedor, use a ferramenta LodCtr para gravar o nome do arquivo binário que contém as cadeias de caracteres de recurso localizadas e as IDs de recurso no Registro. Para obter detalhes sobre como usar LodCtr, consulte [Esquema de contadores de desempenho](performance-counters-schema.md).

5. Ao desinstalar o provedor, use a ferramenta UnlodCtr para remover as informações do provedor do Registro.
