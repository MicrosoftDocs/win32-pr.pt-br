---
description: Lista os identificadores usados pela API SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Identificadores SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753728"
---
# <a name="sspi-handles"></a><span data-ttu-id="bd487-103">Identificadores SSPI</span><span class="sxs-lookup"><span data-stu-id="bd487-103">SSPI Handles</span></span>

<span data-ttu-id="bd487-104">O SSPI usa os seguintes tipos de identificador e ponteiro para esses identificadores:</span><span class="sxs-lookup"><span data-stu-id="bd487-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="bd487-105">**SecHandle** e **PSecHandle**</span><span class="sxs-lookup"><span data-stu-id="bd487-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="bd487-106">**CredHandle** e **PCredHandle**</span><span class="sxs-lookup"><span data-stu-id="bd487-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="bd487-107">**CtxtHandle** e **PCtxtHandle**</span><span class="sxs-lookup"><span data-stu-id="bd487-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="bd487-108">Esses tipos de identificador e ponteiros para esses tipos de identificador são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="bd487-108">These handle types and pointers to these handle types are defined as follows.</span></span>


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



