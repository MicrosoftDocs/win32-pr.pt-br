---
description: A TAPI 1,4 adicionou várias APIs, mensagens, constantes e elementos de estrutura à especificação de 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921690"
---
# <a name="tapi-14"></a><span data-ttu-id="b0c44-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="b0c44-103">TAPI 1.4</span></span>

<span data-ttu-id="b0c44-104">A TAPI 1,4 adicionou várias APIs, mensagens, constantes e elementos de estrutura à especificação de 1,3.</span><span class="sxs-lookup"><span data-stu-id="b0c44-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="b0c44-105">A TAPI 1,4 dá suporte apenas a TSPs de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b0c44-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="b0c44-106">No entanto, ele permite que os aplicativos de 32 bits sejam desenvolvidos sem a necessidade de se preocupar com as limitações do Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b0c44-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="b0c44-107">Os arquivos de cabeçalho TAPI e TSPI são usados para desenvolver ambos os aplicativos para TAPI 1,4 e TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="b0c44-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="b0c44-108">Embora não haja muitas alterações nas estruturas entre essas duas especificações, houve alterações na API (especificamente, suporte a Unicode) que tornam muito importante observar que os cabeçalhos são compilados de forma diferente, dependendo da \_ constante da versão atual da TAPI \_ .</span><span class="sxs-lookup"><span data-stu-id="b0c44-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="b0c44-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b0c44-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="b0c44-110">\_ \_ A versão atual da TAPI deve ser definida para todos os aplicativos TAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c44-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="b0c44-111">Embora não seja estritamente necessário para o desenvolvimento da TAPI 2. x, podem ocorrer alterações futuras para exigir isso.</span><span class="sxs-lookup"><span data-stu-id="b0c44-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



