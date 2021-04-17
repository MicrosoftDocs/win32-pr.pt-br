---
description: CSingleFilterTerminal é uma classe base de terminal adicional aplicável a terminais estáticos e dinâmicos.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: CSingleFilterTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760166"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="fe4d0-103">CSingleFilterTerminal</span><span class="sxs-lookup"><span data-stu-id="fe4d0-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="fe4d0-104">**CSingleFilterTerminal** é uma classe base de terminal adicional aplicável a terminais estáticos e dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="fe4d0-105">Ele é derivado de [**CBaseTerminal**](cbaseterminal.md) e torna a implementação mais específica supondo que o terminal tenha um único filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="fe4d0-106">Quando essa condição é atendida, derivar uma implementação de terminal de **CSingleFilterTerminal** é muito mais fácil do que derivar de **CBaseTerminal**.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="fe4d0-107">Definido em MSPterm. h.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-107">Defined in MSPterm.h.</span></span>

 

 



