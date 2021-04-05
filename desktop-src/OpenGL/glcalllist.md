---
title: função glCallList (GL. h)
description: A função glCallList executa uma lista de exibição.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- função glCallList OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085706"
---
# <a name="glcalllist-function"></a><span data-ttu-id="db3a3-104">função glCallList</span><span class="sxs-lookup"><span data-stu-id="db3a3-104">glCallList function</span></span>

<span data-ttu-id="db3a3-105">A função **glCallList** executa uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="db3a3-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3a3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db3a3-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="db3a3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db3a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3a3-108">*list*</span><span class="sxs-lookup"><span data-stu-id="db3a3-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="db3a3-109">O nome inteiro da lista de exibição a ser executada.</span><span class="sxs-lookup"><span data-stu-id="db3a3-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3a3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db3a3-110">Return value</span></span>

<span data-ttu-id="db3a3-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="db3a3-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db3a3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="db3a3-112">Remarks</span></span>

<span data-ttu-id="db3a3-113">Invocar a função **glCallList** começa a execução da lista de exibição nomeada.</span><span class="sxs-lookup"><span data-stu-id="db3a3-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="db3a3-114">As funções salvas na lista de exibição são executadas na ordem, assim como se você as chamou sem usar uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="db3a3-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="db3a3-115">Se a *lista* não tiver sido definida como uma lista de exibição, **glCallList** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="db3a3-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="db3a3-116">A função **glCallList** pode aparecer dentro de uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="db3a3-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="db3a3-117">Para evitar a possibilidade de recursão infinita resultante de listas de exibição chamando uma outra, um limite é colocado no nível de aninhamento das listas de exibição durante a execução da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="db3a3-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="db3a3-118">No entanto, esse limite é pelo menos 64, dependendo da implementação.</span><span class="sxs-lookup"><span data-stu-id="db3a3-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="db3a3-119">O estado OpenGL não é salvo e restaurado em uma chamada para **glCallList**.</span><span class="sxs-lookup"><span data-stu-id="db3a3-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="db3a3-120">Assim, as alterações feitas no estado OpenGL durante a execução de uma lista de exibição permanecem depois que a execução da lista de exibição é concluída.</span><span class="sxs-lookup"><span data-stu-id="db3a3-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="db3a3-121">Para preservar o estado do OpenGL entre chamadas **glCallList** , use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="db3a3-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="db3a3-122">Você pode executar listas de exibição entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md), desde que a lista de exibição inclua apenas funções que são permitidas nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="db3a3-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="db3a3-123">As funções a seguir recuperam informações relacionadas ao **glCallList**:</span><span class="sxs-lookup"><span data-stu-id="db3a3-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="db3a3-124">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ aninhamento de lista de glGet com Argument GL Max \_</span><span class="sxs-lookup"><span data-stu-id="db3a3-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="db3a3-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="db3a3-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="db3a3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db3a3-126">Requirements</span></span>



| <span data-ttu-id="db3a3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3a3-127">Requirement</span></span> | <span data-ttu-id="db3a3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="db3a3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db3a3-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db3a3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db3a3-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db3a3-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db3a3-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db3a3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db3a3-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db3a3-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db3a3-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="db3a3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="db3a3-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3a3-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="db3a3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db3a3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="db3a3-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db3a3-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="db3a3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="db3a3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db3a3-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db3a3-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3a3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="db3a3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3a3-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="db3a3-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="db3a3-141">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="db3a3-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="db3a3-142">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="db3a3-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="db3a3-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="db3a3-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="db3a3-144">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="db3a3-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="db3a3-145">**glGet**</span><span class="sxs-lookup"><span data-stu-id="db3a3-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="db3a3-146">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="db3a3-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="db3a3-147">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="db3a3-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="db3a3-148">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="db3a3-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="db3a3-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="db3a3-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="db3a3-150">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="db3a3-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="db3a3-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="db3a3-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





