---
title: O que há de novo no WER
description: Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Relatório de erros do Windows Relatório de Erros do Windows, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293897"
---
# <a name="whats-new-in-wer"></a>O que há de novo no WER

Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

A lista a seguir resume os novos recursos do WER para o Windows 7 e o Windows Server 2008 R2.

-   Adiciona a capacidade de gerar uma exceção que ignora todos os manipuladores de exceção, encerrando o aplicativo imediatamente e invocando Relatório de Erros do Windows. Para obter detalhes, consulte a função [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .
-   Adiciona a capacidade de registrar um manipulador de exceção fora do processo que o WER chama quando ocorre uma falha para coletar o nome do evento, os parâmetros de relatório e as opções de inicialização de depuração. Para obter detalhes, consulte a função [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .

Funções que foram adicionadas:

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Estruturas que foram adicionadas:

-   [**informações de exceção de tempo de execução do WER \_ \_ \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 e Windows Vista SP1

A lista a seguir resume os novos recursos do WER para Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).

-   O WER pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário (os aplicativos que realizam seus próprios relatórios de falhas personalizados, incluindo aplicativos .NET, não têm suporte). Para obter mais informações, consulte [coletando despejos de User-Mode](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

A lista a seguir resume os novos recursos do Relatório de Erros do Windows (WER) para o Windows Vista:

-   O WER foi estendido além do monitoramento de falhas e de processos sem resposta. O WER inclui suporte para muitos novos tipos de eventos não críticos, como problemas de desempenho. Isso permite que os desenvolvedores aprendam mais sobre as experiências que seus clientes têm com os aplicativos que desenvolveram.
-   Novas funções oferecem aos desenvolvedores a flexibilidade de criar, personalizar e enviar relatórios de problemas. Para obter mais informações, consulte [funções do WER](wer-functions.md).
-   O [Windows Quality Online Services](https://www.microsoft.com/?ref=go) aprimorado fornece aos desenvolvedores acesso às informações do problema que os clientes estão enviando para seus aplicativos e um mecanismo para fornecer soluções a esses clientes.
-   As funções introduzidas pelo Gerenciador de [recuperação e reinicialização](/windows/desktop/Recovery/application-recovery-and-restart-portal) e [reinicialização](/windows/desktop/RstMgr/restart-manager-portal) do aplicativo permitem que os aplicativos recuperem automaticamente as informações e reiniciem em caso de falha crítica. Os desenvolvedores podem usar esses recursos em seus aplicativos para melhorar significativamente a experiência do usuário.
-   **Relatórios de problemas e soluções no Windows Vista ou na central de ações no Windows 7** é o local central para os usuários interagirem com o wer. Os usuários podem verificar se há novas soluções, gerenciar o histórico de relatórios, exibir os detalhes de um relatório de problemas e gerenciar configurações de relatórios, incluindo a habilitação do WER para verificar se há soluções automaticamente, sem interromper o usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Relatório de Erros do Windows](windows-error-reporting.md)
</dt> </dl>

 

 