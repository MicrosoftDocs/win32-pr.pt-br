---
title: Visão geral do Gerenciador de download
description: Visão geral do Gerenciador de download
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, download em tempo real
- lojas online, download em tempo real
- Digite 2 lojas online, download em tempo real
- Lojas online do Windows Media Player, download em segundo plano
- lojas online, download em segundo plano
- tipo 2 lojas online, download em segundo plano
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Download em tempo real
- Download em segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006063"
---
# <a name="download-manager-overview"></a>Visão geral do Gerenciador de download

O Microsoft Windows Media Player fornece painéis de tarefas da loja online que contêm uma janela do navegador hospedado. Por meio das lojas online, os usuários podem interagir com páginas da Web da loja online na Internet.

O Gerenciador de download do Windows Media Player fornece um modelo de objeto que você pode usar para lidar com as tarefas associadas ao download de conteúdo no computador do usuário do Microsoft Serviços de Informações da Internet (IIS) usando o protocolo HTTP. Com o Gerenciador de download, você pode:

-   Gerencie vários downloads simultaneamente como uma coleção.
-   Especifique uma URL para um arquivo e inicie o download usando HTTP.
-   Consulte o estado e o progresso do download.
-   Pausar, retomar ou cancelar um download.
-   Especifique se um download ocorre em segundo plano ou em tempo real. (O download em segundo plano só está disponível no sistema operacional Microsoft Windows XP.) Consulte [sobre o download em segundo plano e em tempo real](#about-background-and-real-time-downloading).
-   Especifique como o conteúdo é exibido na biblioteca. Consulte [sobre a integração da biblioteca](#about-library-integration).

O Gerenciador de download é a solução para baixar conteúdo do código de script em páginas da Web hospedadas. Para baixar conteúdo usando código C++, use o Windows XP Serviço de Transferência Inteligente em Segundo Plano (BITS). Para obter mais informações, consulte [bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Sobre o download em segundo plano e em tempo real

O Gerenciador de download oferece dois tipos de download: em segundo plano e em tempo real. O tipo que você usa cabe a você, e é possível permitir que o usuário selecione o tipo de download também. Se você optar por permitir que o usuário selecione o tipo de download, certifique-se de explicar as diferenças entre os dois tipos disponíveis.

O download em tempo real ocorre de uma só vez. Quando o usuário inicia um download de arquivo, todo o arquivo é transferido para o computador do usuário em um fluxo único e contínuo. O usuário não pode pausar ou, de outra forma, interromper o download. Se o usuário optar por fechar o Windows Media Player antes de o download ser concluído, ele perderá todos os arquivos incompletos e deverá baixá-los desde o início até a aquisição do conteúdo.

A principal vantagem do download em tempo real é que ele permite que o usuário adquira o conteúdo mais rápido do que o download em segundo plano. O download em tempo real está disponível para usuários do Windows XP, mas é o único tipo de download disponível em versões do sistema operacional Windows antes do Windows XP.

O download em segundo plano ocorre de maneira gradual. Quando o usuário inicia um download em segundo plano, partes do arquivo são transferidas para o computador do usuário quando o tempo do processador está disponível. É possível pausar e retomar um download em segundo plano. Se o usuário optar por fechar o Windows Media Player antes de o download em segundo plano ser concluído, a condição de todos os arquivos incompletos será salva e o download poderá continuar em segundo plano, mesmo após a reinicialização do computador.

O download em segundo plano pode demorar mais do que o download em tempo real, pois o processo de download ocorre apenas quando o processador não está executando outras tarefas.

O download em segundo plano só está disponível ao usar o Windows XP.

## <a name="about-library-integration"></a>Sobre a integração de biblioteca

O Windows Media Player pode organizar automaticamente o conteúdo da loja online na biblioteca. Para habilitar isso, você deve especificar um valor para o atributo **WM/ContentDistributor** para cada arquivo de mídia digital. Quando um arquivo de mídia digital é adicionado à biblioteca, o que acontece automaticamente ao usar o Gerenciador de download, o arquivo é listado automaticamente no nó **música adquirida** ou **vídeos comprados** . Por exemplo, se o valor de **WM/ContentDistributor** for "Proseware" e o arquivo de mídia digital contiver música, o conteúdo aparecerá na biblioteca no seguinte local:

Todas as músicas/Proseware adquiridas

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciador de download**](download-manager.md)
</dt> <dt>

[**Downloadcollection. startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




