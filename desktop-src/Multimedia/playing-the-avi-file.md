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
# <a name="playing-the-avi-file"></a>Executando o arquivo AVI

Antes de usar a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ Play**](mci-play.md) , seu aplicativo aloca a memória para a estrutura, inicializa os membros que ele usará e define os sinalizadores correspondentes aos membros usados na estrutura. (Se seu aplicativo não definir um sinalizador para um membro de estrutura, os drivers MCI ignorarão o membro.) Por exemplo, o exemplo a seguir reproduz um filme a partir da posição inicial especificada por **dwFrom** para a posição final especificada por **dwTo**. (Se uma das posições for zero, o exemplo será escrito de forma que a posição não seja usada.)


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



 

 