---
title: Usando o WER
description: A partir do Windows Vista, o Windows fornece um relatório de falhas, sem resposta e falha de kernel, por padrão, sem a necessidade de alterações no aplicativo.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Relatório de Erros do Windows de relatório de erros do Windows, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bed6d11757d7d4e08cd00ac47479e1246f96b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104365831"
---
# <a name="using-wer"></a>Usando o WER

A partir do Windows Vista, o Windows fornece um relatório de falhas, sem resposta e falha de kernel, por padrão, sem a necessidade de alterações no aplicativo. O relatório incluirá informações de minidespejo e despejo de heap, se necessário. Em vez disso, os aplicativos usam a API WER para enviar relatórios de problemas específicos do aplicativo à Microsoft.

Como o Windows relata automaticamente as exceções sem tratamento, o aplicativo não deve lidar com exceções fatais. Se o processo de falha ou não resposta for interativo, o WER exibirá uma interface do usuário informando o usuário do problema. Um aplicativo será considerado sem resposta se não responder a mensagens do Windows por cinco segundos enquanto o usuário estiver tentando interagir com o aplicativo.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Fluxo de Relatório de Erros do Windows para falhas, não resposta e falhas de kernel

O seguinte mostra as etapas que ocorrem para uma falha de aplicativo, não resposta ou falha do kernel.

1.  O evento de problema ocorre.
2.  O sistema operacional invoca o WER.
3.  O WER coleta os dados, cria um relatório e solicita o consentimento do usuário (se necessário).
4.  O WER enviará o relatório para a Microsoft (servidor Watson) se o usuário tiver consentido.
5.  Se o servidor Watson solicitar dados adicionais, o WER coletará os dados e solicitará o consentimento do usuário (se necessário).
6.  Se o aplicativo tiver se registrado para recuperação e reinicialização, o WER executará as funções de retorno de chamada registradas enquanto os dados são compactados e enviados à Microsoft (se o usuário tiver consentido).
7.  Se uma resposta para o problema estiver disponível na Microsoft, o usuário será notificado.

Os aplicativos podem usar as seguintes funções para personalizar o conteúdo do relatório que é enviado à Microsoft. As funções de registro informam ao WER para incluir os arquivos específicos e os blocos de memória no relatório de erros que ele cria.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Fluxo de Relatório de Erros do Windows para relatórios de eventos genéricos

As etapas a seguir mostram como os aplicativos podem obter um relatório de erros para uma condição de erro não fatal.

1.  O evento de problema não fatal ocorre.
2.  O aplicativo reconhece o evento e usa a sequência de chamadas de função a seguir para gerar o relatório.
    1.  Chame a função [**WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) para criar o relatório.
    2.  Chame a função [**WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) para definir os parâmetros do relatório.
    3.  Chame a função [**WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) para adicionar arquivos ao relatório.
    4.  Chame a função [**WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) para adicionar um minidespejo ao relatório (se necessário).
    5.  Chame a função [**WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) para enviar o relatório.
    6.  Chame o [**WerReportCloseHandle**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) para liberar recursos.
3.  Dependendo das opções específicas usadas ao chamar as funções na etapa 2, o WER concluirá o relatório de erros. O WER garantirá que o relatório seja feito de acordo com as políticas definidas pelo usuário. Por exemplo, o WER enviará o relatório para a Microsoft, colocará o relatório em fila e mostrará as interfaces de usuário apropriadas ao usuário.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Excluindo um aplicativo do Relatório de Erros do Windows

Para excluir seu aplicativo do relatório de erros do Windows, use a função [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) . Para restaurar o relatório de erros para seu aplicativo, use a função [**WerRemoveExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) .

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Recuperando dados automaticamente e reiniciando um aplicativo com falha

Um aplicativo pode usar a recuperação e reinicialização do aplicativo para salvar dados e informações de estado antes que o aplicativo seja encerrado devido a uma exceção sem tratamento ou quando o aplicativo para de responder. O aplicativo também será reiniciado, se solicitado. Para obter detalhes, consulte [recuperação e reinicialização do aplicativo](/windows/desktop/Recovery/application-recovery-and-restart-portal).

## <a name="legacy-api"></a>API herdada

Um aplicativo pode relatar uma falha chamando a função [**ReportFault**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) . No entanto, você não deve usar a função **ReportFault** , a menos que tenha um requisito muito específico de que o comportamento do relatório de erros padrão do sistema operacional não possa atender.

Se o relatório de erros estiver habilitado, o sistema exibirá uma caixa de diálogo para o usuário indicando que o aplicativo encontrou um problema e será fechado. Se houver um depurador configurado na chave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AeDebug** , o usuário receberá a opção de iniciar o depurador. O usuário também recebe a opção de enviar um relatório à Microsoft. Se o usuário enviar o relatório, o sistema exibirá outra caixa de diálogo, agradecendo ao usuário pelo relatório e fornecendo um link para mais informações.

O sistema de relatório de erros do dá suporte aos seguintes modos de operação.



| Modo de operação          | Descrição                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Relatórios de memória compartilhada | Se o contexto de segurança do aplicativo for o mesmo que o contexto de segurança do usuário conectado, o sistema de relatórios de erros usará um bloco de memória compartilhada para comunicação. Este modo não pode ser usado com o modo de relatório do manifesto.<br/>                                                                                               |
| Relatório de manifesto      | Se o contexto de segurança do aplicativo não for o mesmo que o contexto de segurança do usuário conectado, o sistema de relatórios de erros usará um arquivo para comunicação. Esse modo também é usado para relatar aplicativos sem resposta e falhas de kernel. Este modo não pode ser usado com o modo de relatório de memória compartilhada.<br/>                      |
| Relatórios da Internet      | O sistema de relatórios de erros envia todos os dados para a Microsoft pela Internet. Este é o modo de operação padrão. Ele não pode ser usado com o modo de relatório corporativo. Esse modo é usado quando não há nenhum caminho de carregamento corporativo especificado pelo administrador.<br/>                                                                     |
| Relatórios corporativos     | O sistema de relatórios de erros envia todos os dados para um compartilhamento de arquivos em vez de carregá-los diretamente para a Microsoft. Isso permite que os gerentes de ti corporativos examinem os dados antes de serem enviados à Microsoft. Esse modo é usado quando há um caminho de carregamento corporativo especificado pelo administrador. Ele não pode ser usado com o modo de relatório da Internet.<br/> |
| Relatórios sem periféricos      | O sistema de relatório de erros não exibirá nenhuma caixa de diálogo para o usuário. Isso permite que os gerentes de ti corporativos coletem relatórios de erros de seus funcionários em todos os momentos. Esse modo é usado quando o relatório é habilitado pelo administrador, mas a notificação é desabilitada. Ele pode ser usado somente com o modo de relatório corporativo.<br/>        |



 

Para excluir seu aplicativo do relatório de erros, use a função [**AddERExcludedApplication**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa) .

 

