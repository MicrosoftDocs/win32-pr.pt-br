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
# <a name="minidump-files"></a><span data-ttu-id="c4f94-103">Arquivos de minidespejo</span><span class="sxs-lookup"><span data-stu-id="c4f94-103">Minidump Files</span></span>

<span data-ttu-id="c4f94-104">Os aplicativos podem produzir arquivos de minidespejo de modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="c4f94-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="c4f94-105">Os aplicativos podem criar arquivos de minidespejo com rapidez e eficiência.</span><span class="sxs-lookup"><span data-stu-id="c4f94-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="c4f94-106">Como os arquivos de minidespejo são pequenos, eles podem ser facilmente enviados pela Internet para o suporte técnico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4f94-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="c4f94-107">Um arquivo de minidespejo não contém tantas informações quanto um arquivo de despejo de memória completo, mas contém informações suficientes para executar operações básicas de depuração.</span><span class="sxs-lookup"><span data-stu-id="c4f94-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="c4f94-108">Para ler um arquivo de minidespejo, você deve ter os arquivos binários e de símbolo disponíveis para o depurador.</span><span class="sxs-lookup"><span data-stu-id="c4f94-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="c4f94-109">As versões atuais do Microsoft Office e do Microsoft Windows criam arquivos de minidespejo com a finalidade de analisar falhas nos computadores dos clientes.</span><span class="sxs-lookup"><span data-stu-id="c4f94-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="c4f94-110">As seguintes funções DbgHelp são usadas com arquivos de minidespejo.</span><span class="sxs-lookup"><span data-stu-id="c4f94-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="c4f94-111">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="c4f94-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="c4f94-112">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="c4f94-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="c4f94-113">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="c4f94-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



