---
title: show urlacl
description: Lista as DACLs para a URL reservada especificada ou todas as URLs reservadas.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- Mostrar HTTP urlacl
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103916827"
---
# <a name="show-urlacl"></a><span data-ttu-id="94307-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="94307-104">show urlacl</span></span>

<span data-ttu-id="94307-105">Lista as DACLs para a URL reservada especificada ou todas as URLs reservadas.</span><span class="sxs-lookup"><span data-stu-id="94307-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="94307-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94307-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="94307-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="94307-108">Especifica a URL totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="94307-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="94307-109">Se não for especificado, implica todas as URLs.</span><span class="sxs-lookup"><span data-stu-id="94307-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="94307-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94307-110">Examples</span></span>

<span data-ttu-id="94307-111">**Mostrar URL do urlacl =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="94307-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="94307-112">**Mostrar URL do urlacl =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="94307-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




