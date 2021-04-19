---
title: Abrindo vários arquivos AVI
description: Abrindo vários arquivos AVI
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- função initAVI
- função termAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105770474"
---
# <a name="opening-multiple-avi-files"></a>Abrindo vários arquivos AVI

Se seu aplicativo abrir vários arquivos, ele deverá incluir rotinas como as funções simples a seguir. O aplicativo usaria a função "initAVI" durante sua inicialização e a função "termAVI" durante seu encerramento. Essas funções simplesmente encapsulam a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 