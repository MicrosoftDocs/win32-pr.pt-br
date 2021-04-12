---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292194"
---
# <a name="iagent"></a><span data-ttu-id="0078e-103">IAgent</span><span class="sxs-lookup"><span data-stu-id="0078e-103">IAgent</span></span>

<span data-ttu-id="0078e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0078e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0078e-105">**IAgent** define uma interface que permite que os aplicativos carreguem caracteres, recebam eventos e verifiquem o estado atual do servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0078e-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="0078e-106">Essas funções também estão disponíveis em [**IAgentEx**](iagentex.md).</span><span class="sxs-lookup"><span data-stu-id="0078e-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="0078e-107">O método getsuspended incluído nas versões anteriores é obsoleto e retorna **false** para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="0078e-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="0078e-108">**Métodos em ordem vtable**</span><span class="sxs-lookup"><span data-stu-id="0078e-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="0078e-109">Métodos IAgent</span><span class="sxs-lookup"><span data-stu-id="0078e-109">IAgent Methods</span></span>                               | <span data-ttu-id="0078e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0078e-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="0078e-111">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="0078e-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="0078e-112">Carrega o arquivo de dados de um caractere.</span><span class="sxs-lookup"><span data-stu-id="0078e-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="0078e-113">**Liberação**</span><span class="sxs-lookup"><span data-stu-id="0078e-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="0078e-114">Descarrega o arquivo de dados de um caractere.</span><span class="sxs-lookup"><span data-stu-id="0078e-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="0078e-115">**Registre-se**</span><span class="sxs-lookup"><span data-stu-id="0078e-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="0078e-116">Registra um coletor de notificação para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0078e-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="0078e-117">**Unegister**</span><span class="sxs-lookup"><span data-stu-id="0078e-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="0078e-118">Cancela o registro do coletor de notificação de um cliente.</span><span class="sxs-lookup"><span data-stu-id="0078e-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="0078e-119">**Getcharacter**</span><span class="sxs-lookup"><span data-stu-id="0078e-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="0078e-120">Retorna a interface IAgentCharacter para um caractere carregado.</span><span class="sxs-lookup"><span data-stu-id="0078e-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




