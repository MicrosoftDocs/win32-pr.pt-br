---
description: A forma mais simples de e/s no Windows Sockets 2 é o bloqueio de e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Bloqueando entrada/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796094"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="c397c-103">Bloqueando entrada/saída</span><span class="sxs-lookup"><span data-stu-id="c397c-103">Blocking Input/Output</span></span>

<span data-ttu-id="c397c-104">A forma mais simples de e/s no Windows Sockets 2 é o bloqueio de e/s.</span><span class="sxs-lookup"><span data-stu-id="c397c-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="c397c-105">Conforme mencionado nos [sinalizadores e modos de atributo de soquete](socket-attribute-flags-and-modes-2.md), os soquetes são criados no modo de bloqueio por padrão.</span><span class="sxs-lookup"><span data-stu-id="c397c-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="c397c-106">Qualquer operação de e/s com um soquete de bloqueio não retornará até que a operação seja totalmente concluída.</span><span class="sxs-lookup"><span data-stu-id="c397c-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="c397c-107">Assim, qualquer thread só pode executar uma operação de e/s por vez.</span><span class="sxs-lookup"><span data-stu-id="c397c-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="c397c-108">Por exemplo, se um thread emitir uma operação de recebimento e nenhum dado estiver disponível no momento, o thread será bloqueado até que os dados se tornem disponíveis e sejam colocados no buffer do thread.</span><span class="sxs-lookup"><span data-stu-id="c397c-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="c397c-109">Embora isso seja simples, não é necessariamente a maneira mais eficiente de executar e/s (Confira [pseudo-bloqueio e bloqueio real](pseudo-vs--true-blocking-2.md) para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="c397c-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



