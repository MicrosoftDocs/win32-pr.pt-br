---
title: Estilos de serialização
description: Há três estilos que você pode usar para manipular identificadores de serialização.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364207"
---
# <a name="serialization-styles"></a><span data-ttu-id="36894-103">Estilos de serialização</span><span class="sxs-lookup"><span data-stu-id="36894-103">Serialization Styles</span></span>

<span data-ttu-id="36894-104">Há três estilos que você pode usar para manipular identificadores de serialização.</span><span class="sxs-lookup"><span data-stu-id="36894-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="36894-105">Eles são:</span><span class="sxs-lookup"><span data-stu-id="36894-105">These are:</span></span>

-   [<span data-ttu-id="36894-106">Serialização de buffer fixa</span><span class="sxs-lookup"><span data-stu-id="36894-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="36894-107">Serialização de buffer dinâmico</span><span class="sxs-lookup"><span data-stu-id="36894-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="36894-108">Serialização incremental</span><span class="sxs-lookup"><span data-stu-id="36894-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="36894-109">Independentemente do estilo usado, você deve criar um identificador de serialização, serializar os dados e, em seguida, liberar o identificador.</span><span class="sxs-lookup"><span data-stu-id="36894-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="36894-110">O estilo é definido quando o programa cria o identificador e define a maneira como um buffer é manipulado.</span><span class="sxs-lookup"><span data-stu-id="36894-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="36894-111">O identificador mantém o contexto apropriado associado a cada um dos três estilos de serialização.</span><span class="sxs-lookup"><span data-stu-id="36894-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




