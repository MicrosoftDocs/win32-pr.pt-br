---
title: Inicializando a página
description: Inicializando a página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Lojas online do Windows Media Player, inicializando páginas
- lojas online, inicializando páginas
- tipo 2 lojas online, inicializando páginas
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Inicializando páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160115"
---
# <a name="initializing-the-page"></a>Inicializando a página

Quando a página da Web é carregada, a função **init** é executada. Esse código primeiro recupera os dados armazenados em uma sessão anterior. Para obter detalhes, consulte [mantendo as informações da sessão](maintaining-session-information.md). Em seguida, ele cria o objeto **DownloadManager** e o armazena na variável global chamada g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



Em seguida, a função conecta o evento **OnColorChange** à função chamada **OnAppColor** e, em seguida, chama a função diretamente para inicializar a cor do plano de fundo. Consulte [correspondência das cores do Windows Media Player](matching-the-windows-media-player-colors.md).

Por fim, a função inicia um temporizador com um intervalo de um segundo e inicializa as caixas de listagem que exibem as coleções de download pendentes e os itens de download. Isso é importante porque pode haver sessões em andamento na última vez em que a loja online foi fechada e essas informações precisam ser exibidas novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de download**](using-the-download-manager.md)
</dt> </dl>

 

 




