---
description: A ilustração a seguir mostra a arquitetura geral de provedores de serviços de telefonia e suas DLLs (bibliotecas de vínculo dinâmico) da interface do usuário associada.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Arquitetura (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14423dba77af1ded38af4a6f2b896e76d28ca2cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792634"
---
# <a name="architecture-telephony-api"></a>Arquitetura (API de telefonia)

A ilustração a seguir mostra a arquitetura geral de provedores de serviços de telefonia e suas DLLs (bibliotecas de vínculo dinâmico) da interface do usuário associada.

![TSPs e DLLs de interface do usuário associadas](images/spuidl01.png)

O provedor de serviços consiste em um mínimo de dois componentes. A DLL do provedor de serviços (designada na ilustração como principal. TSP) é executado no contexto do processo TAPISRV e executa todas as tarefas do provedor de serviços que não estão relacionadas aos elementos da interface do usuário associados a um uso específico do aplicativo do dispositivo (muito provavelmente, em conjunto com componentes de nível inferior não mostrados na ilustração). Mas, ao contrário das versões anteriores da TAPI em que o código de interface do usuário foi integrado ao provedor de serviços (e executado, devido à arquitetura anterior, dentro do contexto do aplicativo), o provedor de serviços agora deve incluir um componente separado que implementa os elementos da interface do usuário.

A DLL de interface do usuário do provedor de serviços deve exportar funções que são chamadas pela TAPI quando o aplicativo chama funções TAPI que geram interface do usuário: [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog), [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit), [**TUISPI \_**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)phoneConfigDialog, [**TUISPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig), [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)e [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Cada uma dessas funções inclui como um parâmetro um ponteiro para uma função de retorno de chamada na TAPI, do tipo [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback), que a DLL da interface do usuário pode usar para se comunicar bidirecionalmente (enviar e receber dados) com a DLL do provedor de serviços em execução no processo TAPISRV. Se o provedor de serviços gerar uma interface do usuário espontaneável, como a caixa de diálogo de **fala/desligamento** Unimodem, em conjunto com qualquer função TSPI para a qual a interface do usuário não é esperada (por exemplo, qualquer função que não tenha um parâmetro *HWND* ), a DLL da interface do usuário deve exportar [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) e [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata).

> [!Note]  
> As funções de geração de interface do usuário do TSPI originais ( [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog), [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit), [**TSPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig), [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)e [**TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)providerRemove) são obsoletas e nunca são chamadas pela TAPI. Portanto, eles não precisam ser exportados pela DLL do provedor de serviços. No entanto, se o provedor de serviços quiser ser listado como um que possa ser adicionado pelo painel de controle de telefonia, um utilitário fornecido com a telefonia do Windows nas versões 1,4 e anteriores, ele deve **Exportar \_ TSPI providerInstall**; se desejar que o botão [**remover**](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) seja habilitado no painel de controle de telefonia quando for selecionado, ele deverá exportar **TSPI \_ providerRemove**; e se desejar que o botão de **configuração** seja habilitado no painel de controle de telefonia quando for selecionado, ele deverá exportar **TSPI \_ providerConfig**. O painel de controle de telefonia verifica a presença dessas funções no arquivo TSP do provedor de serviços para ajustar sua interface do usuário para refletir quais operações podem ser executadas.

 

A DLL do provedor de serviços deve exportar a função [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) que o processo do TAPISRV usa para obter o nome da dll da interface do usuário a ser carregada no processo do aplicativo. Ele deve exportar a função [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) para receber e responder a solicitações da dll da interface do usuário para que os dados sejam exibidos, e ele deve exportar [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) para o processo TAPISRV para informar ao provedor de serviços quando liberar uma associação estabelecida com a finalidade de gerar uma interface do usuário espontanea em conjunto com uma função que não está definida como apresentação da interface do usuário. A DLL do provedor de serviços pode enviar de forma unidirecional dados para a DLL da interface do usuário usando a nova linha de mensagem TSPI [**\_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Como os nomes das funções TSPI e TUISPI são intencionalmente definidos para serem diferentes, a DLL do provedor de serviços e a DLL da interface do usuário podem ser o mesmo arquivo DLL, se desejado. Com a segmentação adequada, isso não resulta necessariamente em nenhum uso desnecessário da memória no contexto do aplicativo e pode simplificar o processo de instalação para provedores de serviços que podem ser implementados no momento em uma única DLL. A TAPI chama apenas as funções que são apropriadas para o contexto no qual a DLL está sendo usada.

O provedor de serviços de telefonia e a DLL de interface do usuário devem ser projetados com o requisito em mente que as funções de interface do usuário podem ser invocadas de vários processos de aplicativos simultaneamente. Eles também devem considerar que o aplicativo e o serviço TAPI sob os quais o provedor de serviços de telefonia está em execução podem estar em computadores separados em uma LAN.

 

 
