---
title: Iniciando os downloads
description: Iniciando os downloads
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player lojas online, gerenciador de Download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Windows Media Player lojas online, iniciando downloads
- lojas online, Iniciando downloads
- Digite 2 lojas online, Iniciando downloads
- Windows Media Player, gerenciador de Download
- Windows Media Player Gerenciador de download
- Gerenciador de download
- Iniciando downloads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995066"
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

 

 




