---
title: API de plug-in do WinRM
description: A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e URIs de recursos com suporte.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916429"
---
# <a name="winrm-plug-in-api"></a>API de plug-in do WinRM

Os plug-ins Gerenciamento Remoto do Windows são DLLs (bibliotecas de vínculo dinâmico) nativas que se conectam e estendem a funcionalidade do WinRM. A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e [*URIs de recursos*](windows-remote-management-glossary.md) com suporte. Depois que os plug-ins são configurados para o serviço WinRM ou Serviços de Informações da Internet (IIS), eles são carregados no host do WinRM ou host do IIS, respectivamente. As solicitações remotas são roteadas para esses pontos de entrada de plug-in para executar operações.

A seção de referência da API de plug-in do WinRM contém informações detalhadas sobre os seguintes elementos de API:

-   [Pontos de entrada de plug-in de autorização](authorization-plug-in-entry-points.md)
-   [Métodos de plug-in de autorização](authorization-plug-in-methods.md)
-   [Pontos de entrada de plug-in de operações](operations-plug-in-entry-points.md)
-   [Métodos de plug-in de operações](operations-plug-in-methods.md)
-   [Estruturas](winrm-plug-in-api-structures.md)

 

 




