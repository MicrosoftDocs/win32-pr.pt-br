---
title: função glGenLists (GL. h)
description: A função glGenLists gera um conjunto contíguo de listas de exibição vazias.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- função glGenLists OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644394"
---
# <a name="glgenlists-function"></a><span data-ttu-id="92183-104">função glGenLists</span><span class="sxs-lookup"><span data-stu-id="92183-104">glGenLists function</span></span>

<span data-ttu-id="92183-105">A função **glGenLists** gera um conjunto contíguo de listas de exibição vazias.</span><span class="sxs-lookup"><span data-stu-id="92183-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="92183-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92183-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="92183-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92183-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92183-108">*range*</span><span class="sxs-lookup"><span data-stu-id="92183-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="92183-109">O número de listas de exibição vazias contíguas a serem geradas.</span><span class="sxs-lookup"><span data-stu-id="92183-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="92183-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="92183-110">Error codes</span></span>

<span data-ttu-id="92183-111">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="92183-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="92183-112">Nome</span><span class="sxs-lookup"><span data-stu-id="92183-112">Name</span></span>                                                                                                  | <span data-ttu-id="92183-113">Significado</span><span class="sxs-lookup"><span data-stu-id="92183-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92183-114"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92183-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="92183-115">o *intervalo* era negativo.</span><span class="sxs-lookup"><span data-stu-id="92183-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="92183-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92183-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="92183-117">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="92183-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="92183-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="92183-118">Remarks</span></span>

<span data-ttu-id="92183-119">A função **glGenLists** tem um argumento, *Range*.</span><span class="sxs-lookup"><span data-stu-id="92183-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="92183-120">Ele retorna um número inteiro *n* , dessa forma, lista de exibição vazia de *intervalo* , chamada *n*, *n* + 1,.</span><span class="sxs-lookup"><span data-stu-id="92183-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="92183-121">.</span><span class="sxs-lookup"><span data-stu-id="92183-121">.</span></span> <span data-ttu-id="92183-122">., *n* + (*Range* -1), são criados.</span><span class="sxs-lookup"><span data-stu-id="92183-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="92183-123">Se *Range* for zero, se não houver nenhum grupo de nomes contíguos de *intervalo* disponíveis, ou se qualquer erro for gerado, nenhuma lista de exibição será gerada e zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="92183-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="92183-124">A função a seguir recupera informações relacionadas a **glGenLists**:</span><span class="sxs-lookup"><span data-stu-id="92183-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="92183-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="92183-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="92183-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92183-126">Requirements</span></span>



| <span data-ttu-id="92183-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="92183-127">Requirement</span></span> | <span data-ttu-id="92183-128">Valor</span><span class="sxs-lookup"><span data-stu-id="92183-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92183-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92183-129">Minimum supported client</span></span><br/> | <span data-ttu-id="92183-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92183-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="92183-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92183-131">Minimum supported server</span></span><br/> | <span data-ttu-id="92183-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92183-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92183-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92183-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="92183-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="92183-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="92183-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92183-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="92183-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92183-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="92183-137">DLL</span><span class="sxs-lookup"><span data-stu-id="92183-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92183-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92183-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92183-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="92183-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92183-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="92183-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="92183-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="92183-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="92183-142">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="92183-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="92183-143">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="92183-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="92183-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="92183-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="92183-145">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="92183-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="92183-146">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="92183-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





