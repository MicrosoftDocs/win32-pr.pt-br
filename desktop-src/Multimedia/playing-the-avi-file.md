---
title: Como tocar o arquivo AVI
description: Como tocar o arquivo AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- Função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038007"
---
# <a name="playing-the-avi-file"></a>Como tocar o arquivo AVI

Antes de usar a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ PLAY,**](mci-play.md) seu aplicativo aloca a memória para a estrutura, inicializa os membros que ela usará e define os sinalizadores correspondentes aos membros usados na estrutura. (Se o aplicativo não definir um sinalizador para um membro da estrutura, os drivers MCI ignorarão o membro.) Por exemplo, o exemplo a seguir reproduz um filme da posição inicial especificada por **dwFrom** para a posição final especificada por **dwTo**. (Se qualquer posição for zero, o exemplo será escrito para que a posição não seja usada.)


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



 

 