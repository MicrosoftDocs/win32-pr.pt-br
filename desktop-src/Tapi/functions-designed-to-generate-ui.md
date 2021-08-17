---
description: Suponha que, para fins de um exemplo, o aplicativo chama a função TAPI lineConfigDialog, que foi projetada para abrir uma caixa de diálogo para permitir a configuração de opções do provedor de serviços relacionadas ao dispositivo de linha especificado.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funções projetadas para gerar interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e7aeda54d4c04a144b2786b56f32d13c51ab39c5274204485151caecc2db1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140609"
---
# <a name="functions-designed-to-generate-ui"></a>Funções projetadas para gerar interface do usuário

Suponha que, para fins de um exemplo, o aplicativo chama a função TAPI [**lineConfigDialog,**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) que foi projetada para abrir uma caixa de diálogo para permitir a configuração de opções do provedor de serviços relacionadas ao dispositivo de linha especificado. Em resposta a essa chamada, a TAPI solicita que TAPISRV chame o provedor [**TSPIUIIdentify \_**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) no provedor de serviços de telefonia, obtendo o nome da DLL da interface do usuário do TSP.

No contexto do aplicativo, a TAPI carrega a DLL da interface do usuário do TSP e chama a função [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) com os parâmetros fornecidos pelo aplicativo e incluindo um ponteiro para a função [*TAPI DllCallbackProc.*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) A DLL da interface do usuário do TSP exibe a caixa de diálogo de configuração, chamando a função *DllCallbackProc* conforme necessário para obter do provedor de serviços de telefonia as informações a serem exibidas. Sempre que a função *DllCallbackProc* é chamada, a TAPI solicita TAPISRV para chamar a função TSPI do provedor de serviços de [**\_ telefoniaGenericDialogData,**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) passando o bloco de parâmetro da DLL da interface do usuário e retornando o bloco de parâmetro para a DLL da interface do usuário. A DLL da interface do usuário transmite todas as alterações de configuração para o provedor de serviços de telefonia chamando *DllCallbackProc*.

Quando a função for concluída, a DLL da interface do usuário retornará de (nesse caso) [**a linha TUISPIConfigDialog. \_**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) A TAPI chama a [**função FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar a DLL da interface do usuário e retorna para o aplicativo.

 

 
