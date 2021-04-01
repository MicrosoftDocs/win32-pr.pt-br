---
title: função gluErrorString (Glu. h)
description: A função gluErrorString produz uma cadeia de caracteres de erro de um código de erro OpenGL ou GLU. A cadeia de caracteres de erro é somente ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- função gluErrorString OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644554"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="a2227-105">função gluErrorString</span><span class="sxs-lookup"><span data-stu-id="a2227-105">gluErrorString function</span></span>

<span data-ttu-id="a2227-106">A função **gluErrorString** produz uma cadeia de caracteres de erro de um código de erro OpenGL ou Glu.</span><span class="sxs-lookup"><span data-stu-id="a2227-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="a2227-107">A cadeia de caracteres de erro é somente ANSI.</span><span class="sxs-lookup"><span data-stu-id="a2227-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2227-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2227-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="a2227-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2227-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2227-110">*errCode*</span><span class="sxs-lookup"><span data-stu-id="a2227-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a2227-111">Um código de erro OpenGL ou GLU.</span><span class="sxs-lookup"><span data-stu-id="a2227-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2227-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2227-112">Remarks</span></span>

<span data-ttu-id="a2227-113">A função **gluErrorString** produz uma cadeia de caracteres de erro de um código de erro OpenGL ou Glu.</span><span class="sxs-lookup"><span data-stu-id="a2227-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="a2227-114">A cadeia de caracteres está em um formato ISO Latin 1.</span><span class="sxs-lookup"><span data-stu-id="a2227-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="a2227-115">Por exemplo, **gluErrorString**(GL \_ sem \_ \_ memória) retorna a cadeia de caracteres "memória insuficiente".</span><span class="sxs-lookup"><span data-stu-id="a2227-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="a2227-116">Os códigos de erro padrão do GLU são GLU \_ Enumeração inválida \_ , glu \_ \_ valor inválido e Glu \_ memória insuficiente \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a2227-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="a2227-117">Algumas outras funções GLU podem retornar códigos de erro especializados por meio de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="a2227-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="a2227-118">Para obter a lista de códigos de erro OpenGL, consulte [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="a2227-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="a2227-119">A função **gluErrorString** produz cadeias de caracteres de erro somente em ANSI.</span><span class="sxs-lookup"><span data-stu-id="a2227-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="a2227-120">Sempre que possível, use **gluErrorStringWIN**, que permite cadeias de caracteres de erro ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="a2227-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="a2227-121">Isso facilita a localização do seu programa para uso com outro idioma.</span><span class="sxs-lookup"><span data-stu-id="a2227-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2227-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2227-122">Requirements</span></span>



| <span data-ttu-id="a2227-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2227-123">Requirement</span></span> | <span data-ttu-id="a2227-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a2227-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2227-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2227-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a2227-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a2227-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a2227-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2227-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a2227-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a2227-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2227-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2227-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2227-130"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2227-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a2227-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2227-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2227-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2227-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2227-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a2227-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2227-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2227-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2227-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2227-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2227-136">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="a2227-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="a2227-137">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="a2227-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="a2227-138">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="a2227-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="a2227-139">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="a2227-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





