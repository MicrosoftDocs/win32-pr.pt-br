---
description: Os tópicos a seguir descrevem os arquivos de símbolo e a funcionalidade fornecida pelas funções DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Sobre DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162694"
---
# <a name="about-dbghelp"></a>Sobre DbgHelp

Os tópicos a seguir descrevem os arquivos de símbolo e a funcionalidade fornecida pelas [funções DbgHelp](dbghelp-functions.md).

-   [Versões do DbgHelp](dbghelp-versions.md)
-   [Arquivos de Símbolo](symbol-files.md)
-   [Tratamento de símbolos](symbol-handling.md)
-   [Servidores de símbolos e armazenamentos de símbolos](symbol-servers-and-symbol-stores.md)
-   [Arquivos de minidump](minidump-files.md)
-   [Servidor de Origem](source-server-and-source-indexing.md)
-   [Suporte atualizado à plataforma](updated-platform-support.md)

Observe que todas [as funções DbgHelp](dbghelp-functions.md) são de thread único. Portanto, chamadas de mais de um thread para essa função provavelmente resultarão em comportamento inesperado ou corrupção de memória. Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.

 

 



