---
title: Usando a recuperação e reinicialização do aplicativo
description: Um aplicativo pode usar a recuperação e reinicialização do aplicativo (ARR) para salvar dados e informações de estado antes que o aplicativo seja encerrado devido a uma exceção sem tratamento ou quando o aplicativo para de responder. O aplicativo também será reiniciado, se solicitado.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823803"
---
# <a name="using-application-recovery-and-restart"></a>Usando a recuperação e reinicialização do aplicativo

Um aplicativo pode usar a recuperação e reinicialização do aplicativo (ARR) para salvar dados e informações de estado antes que o aplicativo seja encerrado devido a uma exceção sem tratamento ou quando o aplicativo para de responder. O aplicativo também será reiniciado, se solicitado.

Quando você se registra para recuperação ou reinicialização, as informações de registro são adicionadas ao processo. [Relatório de erros do Windows (WER)](/windows/desktop/wer/windows-error-reporting) usa as informações de registro para chamar o retorno de chamada de recuperação e reiniciar o aplicativo. Por exemplo, se você se registrar para recuperação e seu aplicativo encontrar uma exceção sem tratamento, o WER exibirá uma caixa de diálogo para o usuário que dá ao usuário a opção de verificar uma solução online, fechar o programa ou depurar o programa. Se o usuário optar por verificar uma solução ou fechar o programa, o WER chamará o retorno de chamada registrado e dará ao aplicativo a oportunidade de salvar dados e informações de estado. Quando a recuperação for concluída, o aplicativo será encerrado.

Se você se registrar para reinicialização e seu aplicativo encontrar uma exceção sem tratamento, o WER exibirá a mesma caixa de diálogo para o usuário, mas dará a opção de reiniciar o programa em vez de fechar o programa. Se você se registrar para recuperação e reinicialização, a recuperação ocorre primeiro; o aplicativo é então encerrado e reiniciado.

Um aplicativo sem resposta é tratado de maneira semelhante. Um aplicativo é considerado sem resposta se não responder a mensagens do Windows por cinco segundos e o usuário tentar interagir com o aplicativo; o usuário verá (não respondendo) na barra de título. O WER é ativado quando o usuário clica no botão fechar sistema.

Você deve se registrar para recuperação ou reinicialização, ou remover o registro, antes que o aplicativo fique sem resposta ou encontre uma exceção sem tratamento. No entanto, em seu retorno de chamada de recuperação, você pode alterar a linha de comando de reinicialização.

Para obter detalhes sobre o registro para recuperação ou reinicialização, consulte os seguintes tópicos:

-   [Registrando para recuperação de aplicativo](registering-for-application-recovery.md)
-   [Registrando para reinicialização do aplicativo](registering-for-application-restart.md)

Para obter exemplos que implementam os recursos de recuperação e reinicialização, consulte os exemplos de AppRecovery e AppRestart no SDK do Windows localizado na \\ pasta WinBase WindowsErrorReporting.

 

 