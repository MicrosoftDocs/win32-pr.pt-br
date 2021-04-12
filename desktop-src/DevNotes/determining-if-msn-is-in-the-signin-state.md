---
description: O exemplo de código a seguir mostra o uso de um objeto mutex para determinar se o MSN Explorer está conectado.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinando se o MSN está no estado de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501027"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Determinando se o MSN está no estado de entrada

O exemplo de código a seguir mostra o uso de um objeto mutex para determinar se o MSN Explorer está conectado. Quando terminar de usar o identificador, certifique-se de chamar a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

> [!Note]  
> Este objeto mutex está disponível para uso na verificação do MSN Explorer 7. *x* status de entrada. Ele pode não estar disponível em versões subsequentes.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
