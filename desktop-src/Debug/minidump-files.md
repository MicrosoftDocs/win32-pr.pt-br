---
description: Os aplicativos podem produzir arquivos de minidespejo de modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de memória.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Arquivos de minidespejo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088958"
---
# <a name="minidump-files"></a>Arquivos de minidespejo

Os aplicativos podem produzir arquivos de minidespejo de modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de memória. Os aplicativos podem criar arquivos de minidespejo com rapidez e eficiência. Como os arquivos de minidespejo são pequenos, eles podem ser facilmente enviados pela Internet para o suporte técnico do aplicativo.

Um arquivo de minidespejo não contém tantas informações quanto um arquivo de despejo de memória completo, mas contém informações suficientes para executar operações básicas de depuração. Para ler um arquivo de minidespejo, você deve ter os arquivos binários e de símbolo disponíveis para o depurador.

As versões atuais do Microsoft Office e do Microsoft Windows criam arquivos de minidespejo com a finalidade de analisar falhas nos computadores dos clientes.

As seguintes funções DbgHelp são usadas com arquivos de minidespejo.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



