---
description: Os identificadores opacos são usados no TSPI para fazer referência às estruturas de dados que representam linhas, telefones e aparências de chamada.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Identificadores opacos e estruturas de dados privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921084"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="57886-103">Identificadores opacos e estruturas de dados privadas</span><span class="sxs-lookup"><span data-stu-id="57886-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="57886-104">Os identificadores opacos são usados no TSPI para fazer referência às estruturas de dados que representam linhas, telefones e aparências de chamada.</span><span class="sxs-lookup"><span data-stu-id="57886-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="57886-105">Eles aparecem como parâmetros para a maioria das funções e retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="57886-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="57886-106">Há poucas funções que se referem ao dispositivo usando um identificador de dispositivo em vez de um identificador opaco.</span><span class="sxs-lookup"><span data-stu-id="57886-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="57886-107">Nesse caso, a referência é para o dispositivo em si, e não para uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="57886-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="57886-108">Funções que funcionam dessa maneira normalmente são aquelas chamadas em tempos de inicialização antecipados antes que as estruturas de dados sejam criadas e identificadores opacos sejam trocados.</span><span class="sxs-lookup"><span data-stu-id="57886-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="57886-109">O provedor de serviços deve decidir como interpretar esses identificadores.</span><span class="sxs-lookup"><span data-stu-id="57886-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="57886-110">Um provedor de serviços normalmente usa o ponteiro para sua estrutura de dados ou para o índice em uma matriz de estruturas de dados como seu identificador opaco.</span><span class="sxs-lookup"><span data-stu-id="57886-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="57886-111">A única restrição é que o provedor de serviços não pode usar o valor 0 como um [HDRVLINE](hdrvline.md), HDRVCALL ou [HDRVPHONE](hdrvphone.md).</span><span class="sxs-lookup"><span data-stu-id="57886-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="57886-112">O valor 0 ou **NULL** para um identificador tem um significado especial em algumas operações.</span><span class="sxs-lookup"><span data-stu-id="57886-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



