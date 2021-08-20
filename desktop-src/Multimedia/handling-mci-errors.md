---
title: Manipulando erros MCI
description: Manipulando erros MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e2f3a9cc3e711db0d26f28c9ac7e3fd0a8c94eec96117a732f8024372bf9de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141018"
---
# <a name="handling-mci-errors"></a>Manipulando erros MCI

Você sempre deve verificar o valor de retorno da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se ele indicar um erro, você poderá usar [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição textual do erro.

O exemplo a seguir passa o código de erro MCI especificado por *dwError* para **mciGetErrorString** e, em seguida, exibe a descrição do erro textual resultante usando a função [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> Para interpretar um valor de retorno de erro [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , mascarar a palavra de ordem superior (a palavra de ordem inferior contém o código de erro). No entanto, se você passar o valor de retorno do erro para [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), deverá passar todo o valor de doubleword.

 

 

 