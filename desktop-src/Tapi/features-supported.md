---
description: A lista a seguir contém os recursos compatíveis com TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164501"
---
# <a name="features-supported"></a><span data-ttu-id="e9cab-103">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="e9cab-103">Features Supported</span></span>

<span data-ttu-id="e9cab-104">A lista a seguir contém os recursos compatíveis com TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="e9cab-104">The following list contains the TAPI MSP supported features.</span></span>

-   <span data-ttu-id="e9cab-105">Implementa um MSP que manipula um único endereço por instância do MSP.</span><span class="sxs-lookup"><span data-stu-id="e9cab-105">Implements an MSP that handles a single address per instance of the MSP.</span></span> <span data-ttu-id="e9cab-106">Vários endereços like são tratados instanciando o MSP várias vezes.</span><span class="sxs-lookup"><span data-stu-id="e9cab-106">Multiple like addresses are handled by instantiating the MSP multiple times.</span></span> <span data-ttu-id="e9cab-107">Isso simplifica muito a implementação do MSP e das classes base.</span><span class="sxs-lookup"><span data-stu-id="e9cab-107">This greatly simplifies the implementation of the MSP and the base classes.</span></span>
-   <span data-ttu-id="e9cab-108">Implementa todas as interfaces MSPI, incluindo [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="e9cab-108">Implements all the MSPI interfaces, including [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>
-   <span data-ttu-id="e9cab-109">Implementa terminais estáticos prontos para uso para áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="e9cab-109">Implements ready-to-use static terminals for both audio and video.</span></span>
-   <span data-ttu-id="e9cab-110">Implementa classes base de terminal genéricas.</span><span class="sxs-lookup"><span data-stu-id="e9cab-110">Implements generic terminal base classes.</span></span> <span data-ttu-id="e9cab-111">Essas classes de base de dados de terminal são usadas pelas implementações de terminais estáticas mencionadas acima e pelas implementações de terminais dinâmicos encontrados no Termmgr.dll.</span><span class="sxs-lookup"><span data-stu-id="e9cab-111">These terminal base classes are used by both the above-mentioned static terminal implementations and the implementations of dynamic terminals that are found in Termmgr.dll.</span></span> <span data-ttu-id="e9cab-112">O MSP também pode usá-los para implementar terminais adicionais.</span><span class="sxs-lookup"><span data-stu-id="e9cab-112">The MSP can also use them to implement additional terminals.</span></span>
-   <span data-ttu-id="e9cab-113">Usa o Gerenciador de terminal para lidar com terminais dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e9cab-113">Uses the Terminal Manager to handle dynamic terminals.</span></span> <span data-ttu-id="e9cab-114">Cria terminais dinâmicos em um thread de trabalho com uma bomba de mensagem (para liberar aplicativos de console de ter que processar mensagens de janela para terminais de renderização de vídeo e para simplificar problemas de sincronização).</span><span class="sxs-lookup"><span data-stu-id="e9cab-114">Creates dynamic terminals on a worker thread with a message pump (to free console applications from having to process window messages for video render terminals and to simplify synchronization issues).</span></span>
-   <span data-ttu-id="e9cab-115">Dá suporte a chamadas que usam um grafo de filtro por fluxo.</span><span class="sxs-lookup"><span data-stu-id="e9cab-115">Supports calls that use a filter graph per stream.</span></span>
-   <span data-ttu-id="e9cab-116">Implementa a manipulação de eventos de grafo.</span><span class="sxs-lookup"><span data-stu-id="e9cab-116">Implements handling of graph events.</span></span>
-   <span data-ttu-id="e9cab-117">Usa as APIs de pool de threads, em conjunto com um thread de trabalho próprio, para manipular eventos.</span><span class="sxs-lookup"><span data-stu-id="e9cab-117">Uses the thread pooling APIs, in conjunction with a worker thread of its own, to handle events.</span></span>
-   <span data-ttu-id="e9cab-118">Usa as APIs de rastreamento do Windows 2000 (originalmente desenvolvidas para o projeto de roteamento) junto com a lógica adicional para fornecer um mecanismo de registro em log genérico e flexível que pode fazer logon simultaneamente em qualquer combinação do seguinte: um usuário ou depurador de modo kernel; uma janela de console separada com mensagens de log separadas por componente; um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="e9cab-118">Uses the tracing APIs of Windows 2000 (originally developed for the Routing project) along with additional logic to provide a flexible, generic logging mechanism that can simultaneously log to any combination of the following: a user or kernel-mode debugger; a separate console window with log messages separated by component; a log file.</span></span>
-   <span data-ttu-id="e9cab-119">Executa threads livres.</span><span class="sxs-lookup"><span data-stu-id="e9cab-119">Runs free-threaded.</span></span>

 

 
