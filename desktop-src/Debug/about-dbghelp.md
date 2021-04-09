---
description: Os tópicos a seguir descrevem arquivos de símbolo e a funcionalidade fornecida pelas funções DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Sobre o DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089020"
---
# <a name="about-dbghelp"></a>Sobre o DbgHelp

Os tópicos a seguir descrevem arquivos de símbolo e a funcionalidade fornecida pelas [funções dbghelp](dbghelp-functions.md).

-   [Versões do DbgHelp](dbghelp-versions.md)
-   [Arquivos de Símbolo](symbol-files.md)
-   [Manipulação de símbolos](symbol-handling.md)
-   [Servidores de símbolos e armazenamentos de símbolos](symbol-servers-and-symbol-stores.md)
-   [Arquivos de minidespejo](minidump-files.md)
-   [Servidor de origem](source-server-and-source-indexing.md)
-   [Suporte atualizado à plataforma](updated-platform-support.md)

Observe que todas as [funções dbghelp](dbghelp-functions.md) são thread único. Portanto, as chamadas de mais de um thread para essa função provavelmente resultarão em um comportamento inesperado ou corrupção de memória. Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.

 

 



