---
description: Demonstra como registrar um verbo que estende o &\# 0034; Sincronizar&\# 0034; e &\# 0034; Compartilhe&\# 0034; verbos na barra de comandos do Windows Explorer.
title: Sincronizar e compartilhar verbos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968200"
---
# <a name="sync-and-share-verbs"></a>Sincronizar e compartilhar verbos

Demonstra como registrar um verbo que estende os verbos de "sincronização" e "compartilhamento" na barra de comandos do Windows Explorer.

Este tópico inclui as seções a seguir.

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Removendo o exemplo](#removing-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo (sincronização):

1.  Navegue até o diretório que contém o `sync.reg` arquivo
2.  Digite `sync.reg ` na linha de comando ou clique duas vezes no ícone para `sync.reg` registrá-lo.
3.  Abra o Windows Explorer e selecione um arquivo.
4.  Clique na opção **sincronizar** na barra de comandos e selecione uma subopção, como **Paint**.

Para executar o exemplo (compartilhamento):

1.  Navegue até o diretório que contém o `share.reg` arquivo.
2.  Digite `share.reg` na linha de comando ou clique duas vezes no ícone para `share.reg` registrá-lo.
3.  Abra o Windows Explorer e selecione um arquivo. Clique na opção **compartilhar** na barra de comandos.
4.  Clique na opção **compartilhar com** na barra de comandos e selecione uma subopção, como o **Paint**.

## <a name="removing-the-sample"></a>Removendo o exemplo

Para remover o exemplo (sincronização):

1.  Navegue até o diretório que contém o arquivo Uninstallsync. reg.
2.  Digite `uninstallsync.reg` na linha de comando ou clique duas vezes no ícone para `uninstallsync.reg` .

Para remover o exemplo (compartilhamento):

1.  Navegue até o diretório que contém o arquivo Uninstallshare. reg.
2.  Digite `uninstallshare.reg` na linha de comando ou clique duas vezes no ícone para `uninstallshare.reg.`

 

 



