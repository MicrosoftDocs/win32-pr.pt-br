---
title: Usando o Gerenciador de download
description: Usando o Gerenciador de download
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364451"
---
# <a name="using-the-download-manager"></a>Usando o Gerenciador de download

O SDK do Windows Media Player inclui uma página da Web de exemplo que demonstra o uso do Gerenciador de download para baixar arquivos para o computador do usuário. Você pode localizar o exemplo na pasta chamada página da Web em que você instalou o SDK. O nome do arquivo é Sample. ASP. O exemplo fornece a seguinte funcionalidade:

-   Cria o objeto **DownloadManager** .
-   Cria um objeto **downloadcollection** .
-   Inicia o download de cinco arquivos quando o usuário clica em **baixar**. Os caminhos de arquivo padrão são fornecidos no exemplo. Você deve substituir esses caminhos padrão por locais de arquivos em seu próprio servidor. Você pode alterar os caminhos alterando os valores atribuídos à matriz global chamada g \_ sFiles.
-   Mostra informações de status de um download quando o usuário o seleciona.
-   Fornece controles para pausar, retomar, cancelar e remover um item de download.
-   Mantém informações sobre o download de coleções entre sessões usando cookies. Isso é importante porque o usuário pode fechar o Player a qualquer momento. Além disso, se o usuário alternar os painéis de tarefas no Player, a sessão da loja online será encerrada.
-   Usa o download em tempo real por padrão. Você pode alterar o comportamento para download em segundo plano alterando o valor da variável chamada g \_ sDLType. O download em segundo plano está disponível para uso com o sistema operacional Microsoft Windows XP.
-   Sincroniza a cor do plano de fundo com a cor do jogador. Você pode usar esse recurso para fazer com que sua loja online altere a aparência quando o usuário optar por alterar a cor do Player.

As seções a seguir fornecem mais informações:

-   [Inicializando a página](initializing-the-page.md)
-   [Iniciando os downloads](starting-the-downloads.md)
-   [Recuperando informações de status](retrieving-status-information.md)
-   [Mantendo informações da sessão](maintaining-session-information.md)
-   [Depurando a página](debugging-the-page.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




