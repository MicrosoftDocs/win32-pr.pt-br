---
title: show cachestate
description: Lista todos os recursos e suas propriedades associadas que são armazenadas em cache no cache de resposta HTTP ou exibe um único recurso e suas propriedades associadas.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- Mostrar HTTPstate de cache
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293451"
---
# <a name="show-cachestate"></a><span data-ttu-id="71f45-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="71f45-104">show cachestate</span></span>

<span data-ttu-id="71f45-105">Lista todos os recursos e suas propriedades associadas que são armazenadas em cache no cache de resposta HTTP ou exibe um único recurso e suas propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="71f45-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="71f45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71f45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f45-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL = \] ***cadeia de caracteres***\]**</span><span class="sxs-lookup"><span data-stu-id="71f45-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="71f45-108">URL totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="71f45-108">Fully qualified URL.</span></span> <span data-ttu-id="71f45-109">Se não for especificado, implica todas as URLs.</span><span class="sxs-lookup"><span data-stu-id="71f45-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="71f45-110">A URL também pode ser um prefixo para URLs registradas.</span><span class="sxs-lookup"><span data-stu-id="71f45-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="71f45-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71f45-111">Examples</span></span>

<span data-ttu-id="71f45-112">**Mostrar URL de CacheState =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="71f45-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




