---
description: Use o procedimento a seguir para depurar especialistas escritos em Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depurando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdd54484d8dc7d36bf1162433fc98d7d72565d9810c7e0ed838e9193510ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064136"
---
# <a name="debugging-an-expert"></a>Depurando um especialista

Use o procedimento a seguir para depurar especialistas escritos em Microsoft Visual C++.

**Depurando um especialista**

1.  Instale o especialista (arquivo DLL) e o arquivo de banco de dados do programa (. pdb) gerado quando você compilou o especialista no local correto. Para obter mais detalhes, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Iniciar Microsoft Visual C++.
3.  No menu **arquivo** , clique em **abrir** e selecione o nome da sua DLL de especialista.
4.  depois que Microsoft Visual C++ for carregado, clique no menu **Project** e, em seguida, clique em **Configurações**.
5.  Clique em **depurar**. Em **executável para sessão de depuração**, digite o caminho completo de Netmon.exe, por exemplo:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Defina os pontos de interrupção no seu código.

 

 



