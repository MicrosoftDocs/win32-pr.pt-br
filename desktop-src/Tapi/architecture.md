---
description: A ilustração a seguir mostra a arquitetura geral dos provedores de serviços de telefonia e suas DLLs (bibliotecas de vínculo dinâmico) da interface do usuário associadas.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Arquitetura (API de Telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d37c2911a664fee2670a41444ee01e4390c8ee5dd526bf550b75eab4990009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871970"
---
# <a name="architecture-telephony-api"></a>Arquitetura (API de Telefonia)

A ilustração a seguir mostra a arquitetura geral dos provedores de serviços de telefonia e suas DLLs (bibliotecas de vínculo dinâmico) da interface do usuário associadas.

![tsps e dlls de interface do usuário associadas](images/spuidl01.png)

O provedor de serviços consiste em um mínimo de dois componentes. A DLL do provedor de serviços (designada na ilustração como MAIN. O TSP) é executado no contexto do processo TAPISRV e executa todas as tarefas do provedor de serviços que não estão relacionadas aos elementos de interface do usuário associados ao uso do dispositivo por um aplicativo específico (provavelmente, em conjunto com componentes de nível inferior não mostrados na ilustração). Mas, ao contrário das versões anteriores do TAPI em que o código de interface do usuário foi integrado ao provedor de serviços (e executado, devido à arquitetura anterior, dentro do contexto do aplicativo), o provedor de serviços agora deve incluir um componente separado que implementa os elementos de interface do usuário.

A DLL da interface do usuário do provedor de serviços deve exportar funções que são chamadas pela TAPI quando o aplicativo chama funções TAPI que geram interface do usuário: [**tuispi \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog), [**linha TUISPIConfigDialogEdit, \_**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) [**telefone TUISPIConfigDialog \_**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog), [**provedor TUISPIConfig, \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig) [**provedor TUISPIInstall \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)e [**provedor TUISPIRemove \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Cada uma dessas funções inclui como parâmetro um ponteiro para uma função de retorno de chamada na TAPI, do tipo [**TUISPIDLLCALLBACK,**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)que a DLL da interface do usuário pode usar para se comunicar bidirecionalmente (enviar e receber dados) com a DLL do provedor de serviços em execução no processo TAPISRV. Se o provedor de serviços já gerar uma interface do usuário abrangente, como a caixa de diálogo **Unimodem Talk/Hangup,** em conjunto com qualquer função TSPI para a qual a interface do usuário não é esperada (por exemplo, qualquer função que não tenha um parâmetro *hwnd),* a DLL da interface do usuário deverá exportar o provedor [**DE TUISPIGenericDialog \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) e o provedor [**TUISPIGenericDialogData. \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)

> [!Note]  
> As funções de geração de interface do usuário TSPI originais ( [**TSPI \_ lineConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog) [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit), [**TSPI \_ phoneConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog) [**TSPI \_ providerConfig,**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)e [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)) são obsoletas e nunca chamadas pela TAPI. Portanto, eles não precisam ser exportados pela DLL do provedor de serviços. No entanto, se o provedor de serviços quiser ser listado como um que pode ser adicionado pelo serviço de telefonia Painel de Controle, um utilitário fornecido com a Telefonia do Windows [](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) nas versões 1.4 e anteriores, ele deve exportar o provedor **TSPIInstalar \_**; se quiser habilitar o botão Remover no Painel de Controle telefonia quando estiver selecionado, ele deverá exportar o provedor  **TSPIRemove \_** e, se quiser que o botão Instalação seja habilitado no Painel de Controle telefonia quando estiver selecionado, ele deverá exportar o provedor **TSPIConfig \_**. O Painel de Controle de telefonia verifica a presença dessas funções no arquivo TSP do provedor de serviços para ajustar sua interface do usuário para refletir quais operações podem ser executadas.

 

A DLL do provedor de serviços deve exportar a função [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) que o processo TAPISRV usa para obter o nome da DLL da interface do usuário a ser carregada no processo do aplicativo. Ele deve exportar a função [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) para receber e responder a solicitações da DLL da interface do usuário para exibição de dados e deve exportar o provedor [**TSPIFreeDialogInstance \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) para o processo TAPISRV para dizer ao provedor de serviços quando liberar uma associação estabelecida com a finalidade de gerar a interface do usuário em conjunto com uma função que não está definida como apresentar a interface do usuário ao usuário. A DLL do provedor de serviços pode enviar dados unidirecionalmente para a DLL da interface do usuário usando a nova mensagem TSPI [**LINE \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Como os nomes das funções TSPI e TUISPI são intencionalmente definidos como diferentes, a DLL do provedor de serviços e a DLL da interface do usuário podem ser o mesmo arquivo DLL, se desejado. Com a segmentação adequada, isso não necessariamente resulta em qualquer uso desnecessário de memória no contexto do aplicativo e pode simplificar o processo de instalação para provedores de serviços que atualmente podem ser implementados em uma única DLL. A TAPI chama apenas as funções apropriadas para o contexto no qual a DLL está sendo usada.

O provedor de serviços de telefonia e a DLL da interface do usuário devem ser projetados com o requisito em mente de que as funções de interface do usuário podem ser invocadas de vários processos de aplicativo simultaneamente. Eles também devem considerar que o aplicativo e o serviço TAPI sob o qual o provedor de serviços de telefonia está em execução podem estar em computadores separados em uma LAN.

 

 
