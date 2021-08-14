---
description: Os aplicativos podem produzir arquivos de minidump no modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de falha.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Arquivos de minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406086"
---
# <a name="minidump-files"></a>Arquivos de minidump

Os aplicativos podem produzir arquivos de minidump no modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de falha. Os aplicativos podem criar arquivos de minidump de maneira muito rápida e eficiente. Como os arquivos de minidump são pequenos, eles podem ser facilmente enviados pela Internet para suporte técnico para o aplicativo.

Um arquivo de minidump não contém informações como um arquivo de despejo de falha completo, mas contém informações suficientes para executar operações básicas de depuração. Para ler um arquivo de minidump, você deve ter os binários e os arquivos de símbolo disponíveis para o depurador.

As versões atuais do Microsoft Office e do Microsoft Windows criam arquivos de minidump com a finalidade de analisar falhas nos computadores dos clientes.

As funções DbgHelp a seguir são usadas com arquivos de minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



