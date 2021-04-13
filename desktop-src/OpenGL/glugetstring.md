---
title: função gluGetString (Glu. h)
description: A função gluGetString Obtém uma cadeia de caracteres que descreve o número de versão do GLU ou as chamadas de extensão GLU com suporte.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- função gluGetString OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369517"
---
# <a name="glugetstring-function"></a><span data-ttu-id="433a0-104">função gluGetString</span><span class="sxs-lookup"><span data-stu-id="433a0-104">gluGetString function</span></span>

<span data-ttu-id="433a0-105">A função **gluGetString** Obtém uma cadeia de caracteres que descreve o número de versão do Glu ou as chamadas de extensão Glu com suporte.</span><span class="sxs-lookup"><span data-stu-id="433a0-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="433a0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433a0-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="433a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="433a0-108">*name*</span><span class="sxs-lookup"><span data-stu-id="433a0-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="433a0-109">O número de versão do GLU ( \_ versão Glu) ou as chamadas de extensão específicas do fornecedor disponíveis ( \_ extensões Glu).</span><span class="sxs-lookup"><span data-stu-id="433a0-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="433a0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="433a0-110">Remarks</span></span>

<span data-ttu-id="433a0-111">A função **gluGetString** retorna um ponteiro para uma cadeia de caracteres estática, terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="433a0-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="433a0-112">Quando *Name* for Glu \_ version, a cadeia de caracteres retornada será um valor que representa o número de versão de Glu.</span><span class="sxs-lookup"><span data-stu-id="433a0-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="433a0-113">O formato do número de versão é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="433a0-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="433a0-114">O número de versão tem o formato " \_ número principal. \_ número secundário" ou " \_ número principal. \_ número secundário. \_ número de versão".</span><span class="sxs-lookup"><span data-stu-id="433a0-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="433a0-115">As informações específicas do fornecedor são opcionais, e o formato e o conteúdo dependem da implementação.</span><span class="sxs-lookup"><span data-stu-id="433a0-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="433a0-116">Quando *Name* é GLU \_ Extensions, a cadeia de caracteres retornada contém uma lista de nomes de extensões de Glu com suporte que são separadas por espaços.</span><span class="sxs-lookup"><span data-stu-id="433a0-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="433a0-117">O formato da lista de nomes retornada é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="433a0-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="433a0-118">Os nomes de extensão não podem conter espaços.</span><span class="sxs-lookup"><span data-stu-id="433a0-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="433a0-119">A função **gluGetString** é válida para o GLU versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="433a0-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="433a0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433a0-120">Requirements</span></span>



| <span data-ttu-id="433a0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="433a0-121">Requirement</span></span> | <span data-ttu-id="433a0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="433a0-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="433a0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="433a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="433a0-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="433a0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="433a0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="433a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="433a0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="433a0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="433a0-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="433a0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="433a0-128"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="433a0-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="433a0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="433a0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="433a0-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="433a0-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="433a0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="433a0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="433a0-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="433a0-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 





