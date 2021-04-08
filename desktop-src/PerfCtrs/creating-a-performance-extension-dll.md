---
description: Um provedor é uma DLL de desempenho que fornece dados de contador aos consumidores.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Criando uma DLL de extensão de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828392"
---
# <a name="creating-a-performance-extension-dll"></a>Criando uma DLL de extensão de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método também.

Um [provedor v1](providing-counter-data.md) usa uma DLL de desempenho que fornece dados de contador aos consumidores. A DLL de desempenho deve exportar as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) . Normalmente, você usa um arquivo de definição de módulo (. def) para exportar as funções da DLL. O sistema chama essas funções quando um consumidor consulta dados de desempenho.

Na primeira vez que um consumidor chama [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)ou se o consumidor usa a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) ou [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir `HKEY_PERFORMANCE_DATA` , o sistema chama a função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) para cada provedor [registrado](adding-performance-counters.md) no computador. A exceção é se o provedor especificar a lista de objetos que ele suporta na `[objects]` seção do. Arquivo INI. Nesse caso, o sistema chamará o provedor somente se um dos objetos consultados corresponder a um objeto da lista.

A função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) dá a cada provedor uma oportunidade de inicializar suas estruturas de dados de desempenho. Em seguida, se a função **OpenPerformanceData** retornar com êxito, o sistema chamará a função [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) do provedor. As chamadas subsequentes para [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) fazem com que o sistema chame a função **CollectPerformanceData** .

Quando o consumidor termina de coletar dados de desempenho, ele especifica `HKEY_PERFORMANCE_DATA` em uma chamada para a função [**falha RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) . Isso faz com que o sistema chame a função [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) para cada provedor. Os provedores são descarregados.

É possível que vários consumidores coletem dados de desempenho ao mesmo tempo. O sistema chama as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) apenas uma vez sempre que a dll é carregada ou descarregada.

> [!Note]
> Não se esqueça de incluir o "C" externo no seu código C++ para impedir que o compilador adicione decorações aos seus nomes de função; caso contrário, o sistema pode falhar ao localizar suas funções.

> [!Note]
> Se ocorrer um erro ao carregar sua DLL de desempenho, localizar suas funções ou chamar suas funções, o sistema desabilitará o provedor para coleções subsequentes dentro do mesmo processo. Além disso, se isso ocorrer durante a execução em um processo privilegiado, o sistema adicionará um valor de **desabilitar contadores de desempenho** à sua chave de **desempenho** para impedir que o provedor seja carregado no futuro.

Para obter mais informações sobre como escrever uma DLL de desempenho, consulte os seguintes tópicos:

- [Implementando a função OpenPerformanceData](implementing-openperformancedata.md)
- [Implementando a função CollectPerformanceData](implementing-collectperformancedata.md)
- [Tratamento de erro na DLL](error-handling-in-the-dll.md)
- [Restringindo o acesso a DLLs de extensão de desempenho](restricting-access-to-performance-extension--dlls.md)
- [Amostras de DLL de desempenho](performance-dll-samples.md)
