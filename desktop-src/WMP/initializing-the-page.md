---
title: Inicializando a página
description: Inicializando a página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player online, Gerenciador de Download
- lojas online, Gerenciador de Download
- tipo 2 lojas online, Gerenciador de Download
- Windows Media Player online, inicializando páginas
- lojas online, inicializando páginas
- tipo 2 lojas online, inicializando páginas
- Windows Media Player,Gerenciador de Download
- Windows Media Player Gerenciador de Download
- Gerenciador de Download
- inicializando páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e929038c45e5f85a640b5c4ce5c86be56957fdb9067624feddf381ab5093623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748161"
---
# <a name="initializing-the-page"></a>Inicializando a página

Quando a página da Web é carregada, a **função Init** é executado. Esse código primeiro recupera todos os dados armazenados em uma sessão anterior. Para obter detalhes, consulte [Mantendo informações de sessão](maintaining-session-information.md). Em seguida, ele cria **o objeto DownloadManager** e o armazena na variável global chamada g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



Em seguida, a função conecta o **evento OnColorChange** à função chamada **OnAppColor** e, em seguida, chama a função diretamente para inicializar a cor da tela de fundo. Consulte [Correspondência das cores Windows Media Player dados.](matching-the-windows-media-player-colors.md)

Por fim, a função inicia um temporizador com um intervalo de um segundo e inicializa as caixas de listagem que exibem as coleções de download e os itens de download pendentes. Isso é importante porque pode haver sessões em andamento na última vez em que a loja online foi fechada e essas informações precisam ser exibidas novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de Download**](using-the-download-manager.md)
</dt> </dl>

 

 




