---
description: Aguardar funções de depuração
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Aguardar funções de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810927"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="d0f3e-103">Aguardar funções de depuração</span><span class="sxs-lookup"><span data-stu-id="d0f3e-103">Wait Debugging Functions</span></span>

<span data-ttu-id="d0f3e-104">O Microsoft DirectShow fornece várias funções para depurar esperas infinitas.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="d0f3e-105">Em compilações de varejo, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionam como suas contrapartes da API do Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, com intervalos de tempo limite infinitos.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="d0f3e-106">Em compilações de depuração, essas funções usam um valor de tempo limite global.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="d0f3e-107">Se o tempo limite expirar, a função acionará uma declaração.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="d0f3e-108">A chave do registro a seguir especifica o valor de tempo limite, em milissegundos:</span><span class="sxs-lookup"><span data-stu-id="d0f3e-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="d0f3e-109">**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ tempo limite do computador local hKey**</span><span class="sxs-lookup"><span data-stu-id="d0f3e-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="d0f3e-110">em que *<DebugRoot>* é o caminho do registro descrito no tópico [depurar funções de saída](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d0f3e-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="d0f3e-111">Se a chave não existir, o valor de tempo limite padrão será infinito.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="d0f3e-112">Você pode usar a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para substituir a entrada do registro.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="d0f3e-113">Função</span><span class="sxs-lookup"><span data-stu-id="d0f3e-113">Function</span></span>                                                       | <span data-ttu-id="d0f3e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0f3e-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="d0f3e-115">**DbgSetWaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="d0f3e-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="d0f3e-116">Define o valor de tempo limite de depuração.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="d0f3e-117">**DbgWaitForMultipleObjects**</span><span class="sxs-lookup"><span data-stu-id="d0f3e-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="d0f3e-118">Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="d0f3e-119">**DbgWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="d0f3e-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="d0f3e-120">Aguarda a um objeto ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="d0f3e-120">Waits for an object to become signaled.</span></span>                         |



 

 

 



