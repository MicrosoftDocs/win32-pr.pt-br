---
title: função glIsList (GL. h)
description: A função gllsList testa a existência da lista de exibição.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- função glIsList OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295855"
---
# <a name="glislist-function"></a><span data-ttu-id="f1d14-104">função glIsList</span><span class="sxs-lookup"><span data-stu-id="f1d14-104">glIsList function</span></span>

<span data-ttu-id="f1d14-105">A função **gllsList** testa a existência da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="f1d14-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d14-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1d14-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="f1d14-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1d14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d14-108">*list*</span><span class="sxs-lookup"><span data-stu-id="f1d14-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d14-109">Um nome de lista de exibição potencial.</span><span class="sxs-lookup"><span data-stu-id="f1d14-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="f1d14-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f1d14-110">Error codes</span></span>

<span data-ttu-id="f1d14-111">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d14-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f1d14-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f1d14-112">Name</span></span>                                                                                                  | <span data-ttu-id="f1d14-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f1d14-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1d14-114"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1d14-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f1d14-115">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f1d14-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f1d14-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1d14-116">Remarks</span></span>

<span data-ttu-id="f1d14-117">A função **gllsList** retornará GL \_ true se *list* for o nome de uma lista de exibição e retornará GL \_ false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f1d14-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1d14-118">Requirements</span></span>



| <span data-ttu-id="f1d14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d14-119">Requirement</span></span> | <span data-ttu-id="f1d14-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d14-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d14-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d14-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d14-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1d14-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f1d14-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d14-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d14-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1d14-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1d14-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f1d14-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d14-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1d14-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f1d14-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1d14-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1d14-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1d14-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1d14-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f1d14-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1d14-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1d14-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d14-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d14-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f1d14-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f1d14-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f1d14-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f1d14-134">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="f1d14-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="f1d14-135">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="f1d14-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="f1d14-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f1d14-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f1d14-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="f1d14-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="f1d14-138">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="f1d14-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





