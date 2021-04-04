---
title: Usando mais de um identificador de contexto por chamada
description: A capacidade de usar matrizes de identificadores de contexto como parâmetros é disponibilizada no Windows Vista e em sistemas operacionais posteriores.
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b1c69dd182bee8f68e7068bcfcef60efd380a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822627"
---
# <a name="using-more-than-one-context-handle-per-call"></a><span data-ttu-id="c3233-103">Usando mais de um identificador de contexto por chamada</span><span class="sxs-lookup"><span data-stu-id="c3233-103">Using More than One Context Handle per Call</span></span>

<span data-ttu-id="c3233-104">A capacidade de usar matrizes de identificadores de contexto como parâmetros é disponibilizada no Windows Vista e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="c3233-104">The ability to use arrays of context handles as parameters is made available in Windows Vista and later operating systems.</span></span> <span data-ttu-id="c3233-105">No entanto, esse recurso deve ser usado com cuidado dentro de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3233-105">However, this feature should be used carefully within an application.</span></span> <span data-ttu-id="c3233-106">Por exemplo, em uma situação em que um identificador de contexto está sendo usado em várias chamadas, ele se torna cada vez mais difícil de controlar seu uso.</span><span class="sxs-lookup"><span data-stu-id="c3233-106">For example, in a situation where a context handle is being used in multiple calls it becomes increasingly difficult to keep track of its use.</span></span>

 

 




