---
title: Ferramentas de log de eventos do Windows
description: O log de eventos do Windows fornece as ferramentas a seguir que você usa para criar seu provedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365792"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="c7f4c-103">Ferramentas de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="c7f4c-103">Windows Event Log Tools</span></span>

<span data-ttu-id="c7f4c-104">O log de eventos do Windows fornece as ferramentas a seguir que você usa para criar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="c7f4c-105">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="c7f4c-105">Tool</span></span>                                                           | <span data-ttu-id="c7f4c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7f4c-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7f4c-107">**Compilador de mensagem (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="c7f4c-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="c7f4c-108">Um utilitário de linha de comando usado para compilar manifestos de instrumentação e arquivos de texto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="c7f4c-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="c7f4c-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="c7f4c-110">Um utilitário de linha de comando usado principalmente para registrar seu provedor no computador.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="c7f4c-111">Você também pode usá-lo para obter informações de metadados sobre o provedor, seus eventos e os canais para os quais ele registra eventos e para consultar eventos de um canal ou arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="c7f4c-112">A ferramenta de WevtUtil.exe está incluída em% windir% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="c7f4c-113">Para obter informações de uso, digite "wevtutil/?"</span><span class="sxs-lookup"><span data-stu-id="c7f4c-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="c7f4c-114">em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-114">at a command prompt.</span></span><br/> <span data-ttu-id="c7f4c-115">Esse comando é limitado aos membros do grupo Administradores e deve ser executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
