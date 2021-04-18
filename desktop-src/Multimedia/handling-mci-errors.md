---
title: Manipulando erros MCI
description: Manipulando erros MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105778549"
---
# <a name="handling-mci-errors"></a><span data-ttu-id="49127-104">Manipulando erros MCI</span><span class="sxs-lookup"><span data-stu-id="49127-104">Handling MCI Errors</span></span>

<span data-ttu-id="49127-105">Você sempre deve verificar o valor de retorno da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49127-105">You should always check the return value of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="49127-106">Se ele indicar um erro, você poderá usar [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição textual do erro.</span><span class="sxs-lookup"><span data-stu-id="49127-106">If it indicates an error, you can use [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) to get a textual description of the error.</span></span>

<span data-ttu-id="49127-107">O exemplo a seguir passa o código de erro MCI especificado por *dwError* para **mciGetErrorString** e, em seguida, exibe a descrição do erro textual resultante usando a função [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="49127-107">The following example passes the MCI error code specified by *dwError* to **mciGetErrorString**, and then displays the resulting textual error description using the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>


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
> <span data-ttu-id="49127-108">Para interpretar um valor de retorno de erro [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , mascarar a palavra de ordem superior (a palavra de ordem inferior contém o código de erro).</span><span class="sxs-lookup"><span data-stu-id="49127-108">To interpret an [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) error return value yourself, mask the high-order word (the low-order word contains the error code).</span></span> <span data-ttu-id="49127-109">No entanto, se você passar o valor de retorno do erro para [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), deverá passar todo o valor de doubleword.</span><span class="sxs-lookup"><span data-stu-id="49127-109">If you pass the error return value to [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), however, you must pass the entire doubleword value.</span></span>

 

 

 