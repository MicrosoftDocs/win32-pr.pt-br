---
description: Suponha que para os fins de um exemplo que o aplicativo chama a função TAPI lineConfigDialog, que foi projetada para abrir uma caixa de diálogo para permitir a configuração das opções do provedor de serviços relacionadas ao dispositivo de linha especificado.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funções projetadas para gerar a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa360effd2a1504d2325be2131c430664f1e7a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920922"
---
# <a name="functions-designed-to-generate-ui"></a>Funções projetadas para gerar a interface do usuário

Suponha que para os fins de um exemplo que o aplicativo chama a função TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) , que foi projetada para abrir uma caixa de diálogo para permitir a configuração das opções do provedor de serviços relacionadas ao dispositivo de linha especificado. Em resposta a essa chamada, a TAPI solicita TAPISRV para chamar o [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) no provedor de serviços de telefonia, obtendo o nome da dll da interface do usuário do tsp.

No contexto do aplicativo, a TAPI carrega a DLL da interface do usuário do TSP e chama a função [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) com os parâmetros fornecidos pelo aplicativo e inclui um ponteiro para a função [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) TAPI. A DLL da interface do usuário do TSP exibe a caixa de diálogo configuração, chamando a função *DllCallbackProc* conforme necessário para obter do provedor de serviços de telefonia as informações a serem exibidas. Cada vez que a função *DllCallbackProc* é chamada, a TAPI solicita TAPISRV para chamar a função [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) do provedor de serviços de telefonia, passando o bloco de parâmetro do DLL da interface do usuário e retornando o bloco de parâmetro para a DLL da interface do usuário. A DLL da interface do usuário transmite quaisquer alterações de configuração para o provedor de serviços de telefonia chamando *DllCallbackProc*.

Quando a função é concluída, a DLL da interface do usuário retorna de (neste caso) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). A TAPI chama a função [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar a DLL da interface do usuário e retorna para o aplicativo.

 

 
