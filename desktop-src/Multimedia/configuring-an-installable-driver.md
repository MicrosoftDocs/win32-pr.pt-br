---
title: Configurando um driver instalável
description: Configurando um driver instalável
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- drivers instaláveis, configurando
- Configurando drivers instaláveis
- Função OpenDriver
- Função SendDriverMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007378"
---
# <a name="configuring-an-installable-driver"></a>Configurando um driver instalável

Para direcionar um driver instalável para executar tarefas úteis, você deve abrir o driver usando a função [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) e enviar mensagens de ti usando a função [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) . O exemplo a seguir mostra como direcionar o driver para exibir sua caixa de diálogo de configuração.


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 