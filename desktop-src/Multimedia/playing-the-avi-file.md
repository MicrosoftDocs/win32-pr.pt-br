---
title: Executando o arquivo AVI
description: Executando o arquivo AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31754bd5f66b455abc76d363c5ff3e5e286e8040
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293915"
---
# <a name="playing-the-avi-file"></a><span data-ttu-id="bb8be-104">Executando o arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="bb8be-104">Playing the AVI File</span></span>

<span data-ttu-id="bb8be-105">Antes de usar a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ Play**](mci-play.md) , seu aplicativo aloca a memória para a estrutura, inicializa os membros que ele usará e define os sinalizadores correspondentes aos membros usados na estrutura.</span><span class="sxs-lookup"><span data-stu-id="bb8be-105">Before using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_PLAY**](mci-play.md) command, your application allocates the memory for the structure, initializes the members it will use, and sets the flags corresponding to the members used in the structure.</span></span> <span data-ttu-id="bb8be-106">(Se seu aplicativo não definir um sinalizador para um membro de estrutura, os drivers MCI ignorarão o membro.) Por exemplo, o exemplo a seguir reproduz um filme a partir da posição inicial especificada por **dwFrom** para a posição final especificada por **dwTo**.</span><span class="sxs-lookup"><span data-stu-id="bb8be-106">(If your application does not set a flag for a structure member, MCI drivers ignore the member.) For example, the following example plays a movie from the starting position specified by **dwFrom** to the ending position specified by **dwTo**.</span></span> <span data-ttu-id="bb8be-107">(Se uma das posições for zero, o exemplo será escrito de forma que a posição não seja usada.)</span><span class="sxs-lookup"><span data-stu-id="bb8be-107">(If either position is zero, the example is written so that the position is not used.)</span></span>


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 