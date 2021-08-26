---
description: Práticas recomendadas para o desempenho de ativar/desativar
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Práticas recomendadas para o desempenho de ativar/desativar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef9e10b0a6fc82be138951d45f811ce1ccf0dbe2222b620cf73d0c272570c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031046"
---
# <a name="best-practices-for-onoff-performance"></a>Práticas recomendadas para o desempenho de ativar/desativar

## <a name="platform"></a>Plataforma

**clientes-** Windows Vista \| Windows 7  
**servidores-** Windows server 2008 \| Windows server 2008 R2  

## <a name="description"></a>Descrição

Os Estados de energia do sistema (ou S-States), conforme definido na especificação ACPI (Advanced Computer Power Interface), são coloquialmente chamados de Estados ligado/desligado, uma vez que a transição de S-State mais comum é um computador ligado e desligado. as diferentes transições de estado ligado/desligado em um sistema que executa o Windows Vista ou Windows 7 são inicialização, suspensão (acpi S3), hibernação (acpi S4) e desligamento.

O bom desempenho durante essas transições ativadas/desativadas não apenas melhora a qualidade percebida de um computador, mas também afeta muito os padrões de uso do computador e a confiabilidade do sistema. Os clientes podem se sentir frustrados por sistemas que levam muito tempo para serem inicializados ou desligados. Os sistemas móveis que têm transições de suspensão e hibernação longas podem desnecessariamente depauperam a vida útil da bateria. Os tempos de desligamento mais longos também podem afetar negativamente a confiabilidade dos sistemas móveis. Por exemplo, eles aumentam o risco de recortes de energia inesperados.

Extensões de sistema como drivers, aplicativos e serviços podem ter um impacto significativo sobre os tempos de transição ligado/desligado. Esta seção aborda algumas das práticas recomendadas que os desenvolvedores de aplicativos e serviços podem seguir para evitar atrasos durante a inicialização, o modo de espera e o desligamento e para garantir uma experiência de usuário responsiva e após a retomada. para obter mais detalhes sobre como identificar problemas de desempenho de on/off usando o Toolkit de desempenho Windows e implementar as recomendações abaixo para seu aplicativo ou serviço, consulte os white papers na seção "Links para outros recursos".

## <a name="best-practices"></a>Práticas Recomendadas

-   Use o Toolkit de desempenho Windows para medir o desempenho durante todas as transições de ligado/desligado.
-   Executar testes de forma controlada e fazer comparações com relação a uma linha de base válida:
    -   Obter uma medida de linha de base em um sistema com o mínimo de extensões do sistema possível
    -   Adicionar aplicativos e serviços um de cada vez
    -   Testar se há regressões inaceitáveis em tempos de transição ligado/desligado
-   Evite usar código gerenciado para aplicativos no caminho de inicialização crítico.
-   Verifique se todos os aplicativos respondem rapidamente às notificações de desligamento (mensagens do WM \_ QUERYENDSESSION e do WM \_ EndSession).
-   Reduza atrasos no caminho de desligamento de serviços e aplicativos minimizando a atividade de CPU, disco e rede em resposta a notificações de desligamento.
-   Evite atrasos no processamento da notificação de suspensão (mensagem do WM \_ POWERBROADCAST).
-   Responda rapidamente a eventos de retomada e minimize o uso da CPU, do disco e da rede após o reinício.
-   Reduza o consumo de recursos do aplicativo após a inicialização.
-   Não inicie aplicativos da chave RunOnce em cada inicialização.
-   Converta todos os serviços não essenciais no início da demanda ou no início do gatilho para disponibilizar os recursos do sistema durante a inicialização.
-   Evite usar grupos de ordem de carregamento para expressar dependências de serviço.
-   Verifique se todos os serviços em execução relatam esse status assim que possível durante a inicialização para evitar o bloqueio do SCM (Gerenciador de controle de serviço).
-   Evite usar código gerenciado para serviços no caminho de inicialização.
-   Não permita que os serviços optem por receber notificações de pré-desligamento e desligamento ( \_ códigos de controle de DESligamento de controle de serviço \_ e de encerramento de controle de serviço \_ \_ ), a menos que seja absolutamente necessário.
-   Verifique se todos os serviços que optaram por receber notificações de desligamento respondem rapidamente ao SCM.
-   Verifique se os serviços não optam por receber notificações de suspensão, a menos que seja absolutamente necessário.
-   Verifique se todos os serviços respondem rapidamente para retomar eventos e minimizar a CPU, o disco e o uso da rede após a retomada.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   -   [Windows Guia de soluções de transições ativar/desativar](/windows-hardware/test/assessments/onoff-transition-performance)
-   [análise de desempenho de transição ativado/desativado do Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows Análise de desempenho](https://msdn.microsoft.com/performance/default.aspx)
-   [Windows documentação de Toolkit de desempenho no MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Windows Fórum de análise de desempenho](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [rastreamento de eventos para Windows no MSDN](../etw/event-tracing-portal.md)

 

 
