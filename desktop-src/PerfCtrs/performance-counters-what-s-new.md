---
description: Esta seção descreve os novos recursos que foram adicionados aos contadores de desempenho para cada versão.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: O que há de novo (contadores de desempenho)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c86a6a9ea644f1c650137cc392a2d54b6e8eedb34881d6b759d7b6c51635d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674696"
---
# <a name="whats-new-with-performance-counters"></a>O que há de novo nos contadores de desempenho

Esta seção descreve os novos recursos que foram adicionados aos contadores de desempenho para cada versão.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

A ferramenta [ctrpp](ctrpp.md) foi alterada para melhorar e simplificar a geração de código. A ferramenta agora gera apenas um arquivo de cabeçalho e de recurso. Se você quiser o comportamento de geração de código antigo (não recomendado), poderá usar o novo `-legacy` argumento.

- Agora você deve especificar os novos `-o` `-rc` argumentos e que especificam o nome e o local do arquivo de cabeçalho e de recurso, respectivamente.
- Você pode usar o argumento New opcional `-prefix` para especificar uma cadeia de caracteres a ser adicionada ao início das variáveis globais e funções definidas no arquivo de cabeçalho gerado.
- Se você precisar atualizar seu manifesto de contadores, o uso da nova geração de código elimina a necessidade de Mesclar sua implementação de retorno de chamada anterior com o novo código gerado, já que os retornos de chamada não são mais incluídos no código gerado.

Um novo `symbol` atributo está disponível para os seguintes elementos de manifesto:

- [operador](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [neutraliza](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

O `symbol` atributo é necessário para o [provedor](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) e [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)e é opcional para o [contador](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). O atributo permite que você forneça um nome simbólico que pode ser usado para fazer referência a cada elemento ao chamar as funções do provedor (por exemplo, você pode usar o nome simbólico do conjunto de contadores ao chamar [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

A arquitetura de contadores de desempenho para fornecer dados do contador foi completamente alterada para esta versão.

Anteriormente, você usou um arquivo INI para definir os dados do contador e implementou uma DLL de desempenho que foi executada no processo do consumidor para fornecer os dados quando um consumidor o solicitou. Essa arquitetura é preterida e não é recomendada para um novo código devido a problemas significativos de desempenho e confiabilidade.

A nova arquitetura usa um manifesto para definir os dados do contador e executa o código no processo do provedor para fornecer os dados quando um consumidor o solicita. Para obter detalhes adicionais, consulte [fornecendo dados do contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).

As seguintes funções foram adicionadas para esta versão:

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

As seguintes estruturas foram adicionadas para esta versão:

- [\_identidade do contador de desempenho \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_informações do contador de desempenho \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [informações do contador de desempenho \_ \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [instância do contador de desempenho \_ \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Para obter uma lista dos elementos XML que você usa em seu manifesto para definir seus contadores, consulte [esquema de contadores de desempenho](performance-counters-schema.md).

Para obter informações sobre a ferramenta de pré-processador CTRPP que analisa seu manifesto e gera o código que você usa como ponto de partida para seu provedor, consulte [ctrpp](ctrpp.md).
