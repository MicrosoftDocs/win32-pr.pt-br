---
title: Novidades no WER
description: Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows relatório de Relatório de Erros do Windows , novidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a15462b38c158dbe323fd355611640102cb1f11ea26e8fef80c593a00cc5152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670624"
---
# <a name="whats-new-in-wer"></a>Novidades no WER

Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

A lista a seguir resume os novos recursos wer para Windows 7 e Windows Server 2008 R2.

-   Adiciona a capacidade de criar uma exceção que ignora todos os manipuladores de exceção, encerrando o aplicativo imediatamente e invocando Relatório de Erros do Windows. Para obter detalhes, consulte [**a função RaiseFailFastException.**](/previous-versions/dd408166(v=vs.85))
-   Adiciona a capacidade de registrar um manipulador de exceção fora do processo que o WER chama quando ocorre uma falha para coletar o nome do evento, os parâmetros de relatório e as opções de início de depuração. Para obter detalhes, consulte a [**função WerRegisterRuntimeExceptionModule.**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)

Funções que foram adicionadas:

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Estruturas que foram adicionadas:

-   [**INFORMAÇÕES DE \_ EXCEÇÃO DO WER RUNTIME \_ \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 e Windows Vista SP1

A lista a seguir resume os novos recursos do WER para Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).

-   O WER pode ser configurado para que despejos de modo de usuário completos sejam coletados e armazenados localmente depois que um aplicativo de modo de usuário falhar (não há suporte para aplicativos que fazem seus próprios relatórios de falhas personalizados, incluindo aplicativos .NET). Para obter mais informações, consulte [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

A lista a seguir resume os novos recursos do Relatório de Erros do Windows (WER) para Windows Vista:

-   O WER foi estendido além do monitoramento de falhas e processos sem resposta. O WER inclui suporte para muitos novos tipos de eventos não críticos, como problemas de desempenho. Isso permite que os desenvolvedores aprendam mais sobre as experiências que seus clientes têm com os aplicativos que desenvolveram.
-   As novas funções oferecem aos desenvolvedores a flexibilidade de criar, personalizar e enviar relatórios de problemas. Para obter mais informações, consulte [Funções WER](wer-functions.md).
-   O Windows [Quality Online Services](https://www.microsoft.com/?ref=go) aprimorado fornece aos desenvolvedores acesso às informações de problema que os clientes estão enviando para seus aplicativos e um mecanismo para fornecer soluções a esses clientes.
-   As funções introduzidas pelo Gerenciador [](/windows/desktop/RstMgr/restart-manager-portal) [de Recuperação](/windows/desktop/Recovery/application-recovery-and-restart-portal) e Reinicialização e Reinicialização de Aplicativos permitem que os aplicativos recuperem automaticamente informações e reiniciem em caso de falha crítica. Os desenvolvedores podem usar esses recursos em seus aplicativos para melhorar significativamente sua experiência do usuário.
-   **Relatórios e soluções de problemas Windows Vista ou** o Centro de Ações no Windows 7 é o local central para os usuários interagirem com o WER. Os usuários podem verificar novas soluções, gerenciar seu histórico de relatórios, exibir os detalhes de um relatório de problemas e gerenciar configurações de relatório, incluindo a habilitação do WER para verificar soluções automaticamente sem interromper o usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Relatório de Erros do Windows](windows-error-reporting.md)
</dt> </dl>

 

 