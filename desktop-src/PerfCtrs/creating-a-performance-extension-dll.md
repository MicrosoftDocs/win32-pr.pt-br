---
description: Um provedor é uma DLL de desempenho que fornece dados de contador aos consumidores.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Criando uma DLL de extensão de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ef4509af77bcc1a4016e494a2834d40162305a837349e32a573cbf36d994d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011314"
---
# <a name="creating-a-performance-extension-dll"></a>Criando uma DLL de extensão de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em Fornecendo dados de contador usando a versão [2.0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e que você migre contadores de desempenho existentes para usar esse método também.

Um [provedor V1 usa](providing-counter-data.md) uma DLL de desempenho que fornece dados de contador aos consumidores. A DLL de desempenho deve exportar as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)e [**ClosePerformanceData.**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) Normalmente, você usa um arquivo de definição de módulo (.def) para exportar as funções da DLL. O sistema chama essas funções quando um consumidor consulta dados de desempenho.

Na primeira vez que um consumidor chamar [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)ou se o consumidor usar a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) ou [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir , o sistema chamará a `HKEY_PERFORMANCE_DATA` função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) para cada provedor registrado no computador. [](adding-performance-counters.md) A exceção será se o provedor especificar a lista de objetos que ele dá suporte na `[objects]` seção do arquivo .INI dados. Nesse caso, o sistema chamará o provedor somente se um dos objetos consultados corresponde a um objeto da lista.

A [**função OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) oferece a cada provedor uma oportunidade de inicializar suas estruturas de dados de desempenho. Em seguida, se a **função OpenPerformanceData** retornar com êxito, o sistema chamará a função [**CollectPerformanceData do**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) provedor. Chamadas subsequentes [**para RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) faz com que o sistema chame a **função CollectPerformanceData.**

Quando o consumidor termina de coletar dados de desempenho, ele especifica em `HKEY_PERFORMANCE_DATA` uma chamada para a função [**RegCloseKey.**](/windows/desktop/api/winreg/nf-winreg-regclosekey) Isso faz com que o sistema chame a [**função ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) para cada provedor. Em seguida, os provedores são descarregados.

É possível que vários consumidores coletem dados de desempenho ao mesmo tempo. O sistema chama [**as funções OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) apenas uma vez sempre que a DLL é carregada ou descarregada.

> [!Note]
> Certifique-se de incluir extern "C" em seu código C++ para impedir que o compilador adicione decorações aos seus nomes de função; caso contrário, o sistema poderá falhar ao encontrar suas funções.

> [!Note]
> Se ocorrer um erro ao carregar sua DLL de desempenho, localizar suas funções ou chamar suas funções, o sistema desabilitará o provedor para coleções subsequentes dentro do mesmo processo. Além disso, se isso ocorrer durante **a** execução em um processo privilegiado,  o sistema adiciona um valor Desabilitar Contadores de Desempenho à sua chave de desempenho para impedir que o provedor seja carregado no futuro.

Para obter mais informações sobre como escrever uma DLL de desempenho, consulte os seguintes tópicos:

- [Implementando a função OpenPerformanceData](implementing-openperformancedata.md)
- [Implementando a função CollectPerformanceData](implementing-collectperformancedata.md)
- [Tratamento de erro na DLL](error-handling-in-the-dll.md)
- [Restringindo o acesso a DLLs de extensão de desempenho](restricting-access-to-performance-extension--dlls.md)
- [Exemplos de DLL de desempenho](performance-dll-samples.md)
