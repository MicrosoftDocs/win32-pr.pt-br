---
title: Usando o Gerenciador de Download
description: Usando o Gerenciador de Download
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player online, Gerenciador de Download
- lojas online, Gerenciador de Download
- tipo 2 lojas online, Gerenciador de Download
- Windows Media Player,Gerenciador de Download
- Windows Media Player Gerenciador de Download
- Gerenciador de Download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a271849e22d17ec406cea24aa0afb92631bf533b39ea2beb45d5cc74b635d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830704"
---
# <a name="using-the-download-manager"></a>Usando o Gerenciador de Download

O Windows Media Player SDK inclui uma página da Web de exemplo que demonstra o uso do Gerenciador de Download para baixar arquivos no computador do usuário. Você pode localizar o exemplo na pasta chamada WebPage em que você instalou o SDK. O nome do arquivo é sample.asp. O exemplo fornece a seguinte funcionalidade:

-   Cria o **objeto DownloadManager.**
-   Cria um **objeto DownloadCollection.**
-   Inicia o download de cinco arquivos quando o usuário clica em **Baixar**. Os caminhos de arquivo padrão são fornecidos no exemplo. Você deve substituir esses caminhos padrão pelos locais dos arquivos em seu próprio servidor. Você pode alterar os caminhos alterando os valores atribuídos à matriz global chamada g \_ sFiles.
-   Mostra informações de status para um download quando o usuário as seleciona.
-   Fornece controles para pausar, retomar, cancelar e remover um item de download.
-   Mantém informações sobre o download de coleções entre sessões usando cookies. Isso é importante porque o usuário pode fechar o Player a qualquer momento. Além disso, se o usuário alterna os painéis de tarefas no Player, a sessão da loja online termina.
-   Usa o download em tempo real por padrão. Você pode alterar o comportamento para download em segundo plano alterando o valor da variável chamada \_ g sDLType. O download em segundo plano está disponível para uso com o sistema operacional Microsoft Windows XP.
-   Sincroniza a cor da tela de fundo com a cor do player. Você pode usar esse recurso para fazer com que sua loja online altere a aparência quando o usuário optar por alterar a cor do Player.

As seções a seguir fornecem mais informações:

-   [Inicializando a página](initializing-the-page.md)
-   [Iniciando os downloads](starting-the-downloads.md)
-   [Recuperando informações de status](retrieving-status-information.md)
-   [Mantendo informações de sessão](maintaining-session-information.md)
-   [Depurando a página](debugging-the-page.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




