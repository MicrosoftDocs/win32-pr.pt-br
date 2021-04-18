---
title: delete cache
description: Libera o cache de URL inteiro ou exclui as entradas de acordo com a URL especificada.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Excluir cache HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105767652"
---
# <a name="delete-cache"></a><span data-ttu-id="49579-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="49579-104">delete cache</span></span>

<span data-ttu-id="49579-105">Libera o cache de URL inteiro ou exclui as entradas de acordo com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="49579-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="49579-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49579-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="49579-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="49579-108">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="49579-108">Required.</span></span> <span data-ttu-id="49579-109">Especifica a URL totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="49579-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="49579-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursivo = \] {Yes \| no}**</span><span class="sxs-lookup"><span data-stu-id="49579-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="49579-111">Em caso afirmativo, remove todas as entradas na URL especificada.</span><span class="sxs-lookup"><span data-stu-id="49579-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="49579-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49579-112">Examples</span></span>

<span data-ttu-id="49579-113">**excluir URL do cache = https://www.contoso.com:80/myresource/ recursivo = Sim**</span><span class="sxs-lookup"><span data-stu-id="49579-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




