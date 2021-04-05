---
description: O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921830"
---
# <a name="cmsparray"></a><span data-ttu-id="41eb4-103">CMSPArray</span><span class="sxs-lookup"><span data-stu-id="41eb4-103">CMSPArray</span></span>

<span data-ttu-id="41eb4-104">O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda.</span><span class="sxs-lookup"><span data-stu-id="41eb4-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="41eb4-105">Ele foi projetado para manter pequenas matrizes com tipos de dados simples.</span><span class="sxs-lookup"><span data-stu-id="41eb4-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="41eb4-106">Ele não tem uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="41eb4-106">It doesn't have a critical section.</span></span> <span data-ttu-id="41eb4-107">Suas únicas dependências são **realloc** e **memmove**.</span><span class="sxs-lookup"><span data-stu-id="41eb4-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="41eb4-108">Ele é usado internamente para manter listas de ponteiros de objeto.</span><span class="sxs-lookup"><span data-stu-id="41eb4-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="41eb4-109">É semelhante à implementação de **CSimpleArray** da ATL, mas é mais eficiente para alocações iniciais.</span><span class="sxs-lookup"><span data-stu-id="41eb4-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="41eb4-110">Esse modelo é definido em MSPutils. h.</span><span class="sxs-lookup"><span data-stu-id="41eb4-110">This template is defined in MSPutils.h.</span></span>

 

 



