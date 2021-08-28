---
description: A partir do TAPI 2.1, as DLLs da interface do usuário do provedor de serviços de telefonia podem ser usadas para gerenciar e exibir caixas de diálogo. A TAPI carrega a DLL no processo de um aplicativo que invoca qualquer uma das funções do provedor de serviços que pode exibir uma caixa de diálogo.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Novidades do TSPI versão 2.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260978ad99bf49ed0beae0e71b2a02a794eef1a7af0c25074c20a08c1da054c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659816"
---
# <a name="whats-new-for-tspi-version-21"></a>Novidades do TSPI versão 2.1

A partir do TAPI 2.1, as DLLs da interface do usuário do provedor de serviços de telefonia podem ser usadas para gerenciar e exibir caixas de diálogo. A TAPI carrega a DLL no processo de um aplicativo que invoca qualquer uma das funções do provedor de serviços que pode exibir uma caixa de diálogo.

A partir do TAPI 2.1, os manipuladores de solicitação de proxy podem ser implementados. Um manipulador é um aplicativo de telefonia completo que normalmente é executado em um servidor de telefonia e fornece serviços que são implementados mais adequadamente em um aplicativo do que um driver.

As funções e mensagens que foram novas ou alteradas para o TSPI versão 2.1 são as seguinte:

-   [**TSPI_lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   **TSPI_lineDropNoOwner**—**obsoleto**
-   **TSPI_lineDropOnClose**—**obsoleto**
-   [**Tspi_linegetid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI_lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI_lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI_lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [**TSPI_lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI_phoneGetID**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [**Tspi_providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [**TSPI_providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   [**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))
-   [**Line_generate**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))
-   [**Line_monitordigits**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))
-   [**Line_monitormedia**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))
-   [**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))
-   [**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))
-   [**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))

A DLL da interface do usuário do provedor de serviços de telefonia fornece um meio de permitir a interação do usuário dentro do contexto do aplicativo em vez do próprio provedor de serviços. O TSPI versão 2.1 entregue as seguintes novas funções, mensagens e estruturas para implementação:

-   [**TSPI_providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [**TSPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [**TSPI_providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [**TUISPI_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [**TUISPI_lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [**TUISPI_phoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [**TUISPI_providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [**TUISPI_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [**TUISPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [**TUISPI_providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [**TUISPI_providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [**LINE_CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
-   [**LINE_SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)

 

 
