---
title: Iniciando os downloads
description: Iniciando os downloads
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, Iniciando downloads
- lojas online, Iniciando downloads
- Digite 2 lojas online, Iniciando downloads
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Iniciando downloads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364383"
---
# <a name="starting-the-downloads"></a>Iniciando os downloads

O download é iniciado quando o usuário clica em **baixar**. Esse botão é denominado btnDownload no código e a função do manipulador de eventos para o evento **onclick** é denominada "ondownload".

"Ondownload" primeiro cria um novo objeto vazio **downloadcollection** e o atribui a uma variável local.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Em seguida, a função inicia cada um dos cinco itens baixando e armazena o objeto **DownloadItem** retornado em uma matriz.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Em seguida, o código atualiza os elementos da interface do usuário com as informações sobre a coleção de download e seus itens de download.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de download**](using-the-download-manager.md)
</dt> </dl>

 

 




