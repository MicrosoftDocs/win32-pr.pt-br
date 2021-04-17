---
title: função glDeleteLists (GL. h)
description: A função glDeleteLists exclui um grupo contíguo de listas de exibição.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- função glDeleteLists OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789880"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="7343e-104">função glDeleteLists</span><span class="sxs-lookup"><span data-stu-id="7343e-104">glDeleteLists function</span></span>

<span data-ttu-id="7343e-105">A função **glDeleteLists** exclui um grupo contíguo de listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="7343e-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="7343e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7343e-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="7343e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7343e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7343e-108">*list*</span><span class="sxs-lookup"><span data-stu-id="7343e-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="7343e-109">O nome inteiro da primeira lista de exibição a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="7343e-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="7343e-110">*range*</span><span class="sxs-lookup"><span data-stu-id="7343e-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="7343e-111">O número de listas de exibição a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="7343e-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7343e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7343e-112">Return value</span></span>

<span data-ttu-id="7343e-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7343e-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7343e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7343e-114">Error codes</span></span>

<span data-ttu-id="7343e-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7343e-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7343e-116">Nome</span><span class="sxs-lookup"><span data-stu-id="7343e-116">Name</span></span>                                                                                                  | <span data-ttu-id="7343e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="7343e-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7343e-118"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7343e-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7343e-119">o *intervalo* era negativo.</span><span class="sxs-lookup"><span data-stu-id="7343e-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="7343e-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7343e-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7343e-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7343e-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7343e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7343e-122">Remarks</span></span>

<span data-ttu-id="7343e-123">A função **glDeleteLists** faz com que um grupo contíguo de listas de exibição seja excluído.</span><span class="sxs-lookup"><span data-stu-id="7343e-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="7343e-124">O parâmetro *list* é o nome da primeira lista de exibição a ser excluída e *Range* é o número de listas de exibição a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="7343e-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="7343e-125">Todas as listas de exibição *d* *com list*  =  *d*  =  *listar*  +  *intervalo* -1 são excluídas.</span><span class="sxs-lookup"><span data-stu-id="7343e-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="7343e-126">Todos os locais de armazenamento alocados para as listas de exibição especificadas são liberados e os nomes estão disponíveis para reutilização posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7343e-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="7343e-127">Os nomes dentro do intervalo que não têm uma lista de exibição associada são ignorados.</span><span class="sxs-lookup"><span data-stu-id="7343e-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="7343e-128">Se o *intervalo* for zero, nada acontecerá.</span><span class="sxs-lookup"><span data-stu-id="7343e-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="7343e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7343e-129">Requirements</span></span>



| <span data-ttu-id="7343e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7343e-130">Requirement</span></span> | <span data-ttu-id="7343e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7343e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7343e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7343e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7343e-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7343e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7343e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7343e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7343e-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7343e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7343e-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7343e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7343e-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7343e-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7343e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7343e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="7343e-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7343e-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7343e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7343e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7343e-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7343e-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7343e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7343e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7343e-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7343e-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7343e-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="7343e-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="7343e-145">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="7343e-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="7343e-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7343e-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7343e-147">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="7343e-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="7343e-148">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="7343e-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="7343e-149">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="7343e-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





