---
title: API de plug-in do WinRM
description: A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e URIs de recursos com suporte.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7359ed212e50b71343ce9a96832060e9ec8121cdf3e11f3f353698e1a4fa9dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742766"
---
# <a name="winrm-plug-in-api"></a>API de plug-in do WinRM

Windows Os plug-ins de gerenciamento remoto são DLLs (bibliotecas de vínculo dinâmico) nativas que se conectam e estendem a funcionalidade do WinRM. A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e [*URIs de recursos*](windows-remote-management-glossary.md) com suporte. depois que os plug-ins são configurados para o serviço winrm ou Serviços de Informações da Internet (IIS), eles são carregados no host do winrm ou host do IIS, respectivamente. As solicitações remotas são roteadas para esses pontos de entrada de plug-in para executar operações.

A seção de referência da API de plug-in do WinRM contém informações detalhadas sobre os seguintes elementos de API:

-   [Pontos de entrada de plug-in de autorização](authorization-plug-in-entry-points.md)
-   [Métodos de plug-in de autorização](authorization-plug-in-methods.md)
-   [Pontos de entrada de plug-in de operações](operations-plug-in-entry-points.md)
-   [Métodos de plug-in de operações](operations-plug-in-methods.md)
-   [Estruturas](winrm-plug-in-api-structures.md)

 

 




