---
description: Suponha que o provedor de serviços deve exibir uma caixa de diálogo (como a caixa de diálogo Unimodem ou ATSP Talk/desligamento) durante o processamento de lineMakeCall ou lineDial.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Funções não projetadas para gerar interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bd7ed1395136d1a2d2a31b060127395e8804ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505865"
---
# <a name="functions-not-designed-to-generate-ui"></a>Funções não projetadas para gerar interface do usuário

Suponha que o provedor de serviços deve exibir uma caixa de diálogo (como a caixa de diálogo Unimodem ou ATSP **Talk/desligamento** ) durante o processamento de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial). Nesse caso, é o provedor de serviços, não o aplicativo, que decide que a interface do usuário deve ser exibida.

Para invocar a DLL de interface do usuário no processo do aplicativo, o provedor de serviços chama o retorno de chamada de [*\_ evento de linha*](/windows/win32/api/tspi/nc-tspi-lineevent) TSPI, gerando uma mensagem [**\_ CREATEDIALOGINSTANCE de linha**](line-createdialoginstance.md) , passando um ponteiro para uma estrutura do tipo [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams). Essa estrutura contém o **dwRequestID** da função com a qual a interface do usuário está associada, permitindo que TAPISRV identifique o aplicativo cliente no qual a interface do usuário deve ser gerada.

O TAPISRV solicita a instância do aplicativo TAPI correta para carregar a DLL da interface do usuário e criar um thread para a interface do usuário dentro do processo do aplicativo. Desse novo thread de interface do usuário, a TAPI chama a função [**TUISPI \_ PROVIDERGENERICDIALOG**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) da dll da interface do usuário, passando dados que foram especificados pelo provedor de serviços de telefonia na estrutura passada com a mensagem [**\_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) Message; a DLL da interface do usuário exibe a caixa de diálogo apropriada (que é uma questão para o design privado entre a DLL da interface do usuário e o provedor de serviços de telefonia). A DLL da interface do usuário não retorna de **TUISPI \_ providerGenericDialog** até que a caixa de diálogo seja fechada.

O provedor de serviços de telefonia pode gerar dados atualizados para exibir na caixa de diálogo (ou, por exemplo, instruir a caixa de diálogo a ser fechada, se a chamada for abandonada ou se outros eventos ocorrerem) enviando uma mensagem de [**\_ SENDDIALOGINSTANCEDATA de linha**](line-senddialoginstancedata.md) . O TAPISRV transmite os dados para a TAPI, que chama a função [**\_ ProviderGenericDialogData do TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) da dll da interface do usuário. Esse mecanismo fornece um "envio" unidirecional para a DLL da interface do usuário. Se a DLL da interface do usuário quiser informar o provedor de serviços de telefonia dos resultados da caixa de diálogo ou obter outros dados, ela poderá chamar a função [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) (um ponteiro para o qual ele recebeu quando [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) for chamado).

Quando a caixa de diálogo é ignorada, [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) retorna à TAPI. A TAPI chama [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar a DLL da interface do usuário e sai do thread de interface do usuário criado no contexto do aplicativo. Em seguida, ele solicita TAPISRV para chamar a função [**\_ providerFreeDialogInstance TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) do provedor de serviços de telefonia para desassociar a associação criada quando o provedor de serviços de telefonia enviou originalmente a [**linha \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) Message. Essa função também será chamada se o processo do aplicativo for encerrado inesperadamente antes de **TUISPI \_ providerGenericDialog** retornar.

 

 
