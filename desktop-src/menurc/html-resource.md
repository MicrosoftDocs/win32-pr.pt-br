---
title: Recurso HTML
description: Define um arquivo HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menus de recursos HTML e outros recursos
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823307"
---
# <a name="html-resource"></a><span data-ttu-id="eaa03-104">Recurso HTML</span><span class="sxs-lookup"><span data-stu-id="eaa03-104">HTML resource</span></span>

<span data-ttu-id="eaa03-105">Define um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="eaa03-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="eaa03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaa03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa03-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="eaa03-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="eaa03-108">Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="eaa03-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="eaa03-109"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="eaa03-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="eaa03-110">O nome do arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="eaa03-110">The name of the HTML file.</span></span> <span data-ttu-id="eaa03-111">Ele deve ser um caminho completo ou relativo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="eaa03-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="eaa03-112">O caminho deve ser uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="eaa03-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eaa03-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eaa03-113">Examples</span></span>

<span data-ttu-id="eaa03-114">O exemplo a seguir define um recurso HTML:</span><span class="sxs-lookup"><span data-stu-id="eaa03-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




