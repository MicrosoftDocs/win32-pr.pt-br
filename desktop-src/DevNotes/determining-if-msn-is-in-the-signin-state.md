---
description: O exemplo de código a seguir mostra o uso de um objeto mutex para determinar se o MSN Explorer está conectado.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinando se o MSN está no estado de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654186"
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



 

 
