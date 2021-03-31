---
title: função glColorMask (GL. h)
description: A função glColorMask habilita e desabilita a gravação de componentes de cores do buffer de quadros.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- função glColorMask OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824260"
---
# <a name="glcolormask-function"></a><span data-ttu-id="f2e16-104">função glColorMask</span><span class="sxs-lookup"><span data-stu-id="f2e16-104">glColorMask function</span></span>

<span data-ttu-id="f2e16-105">A função **glColorMask** habilita e desabilita a gravação de componentes de cores do buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="f2e16-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e16-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e16-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="f2e16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e16-108">*vermelho*</span><span class="sxs-lookup"><span data-stu-id="f2e16-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e16-109">Especifique se o vermelho pode ou não ser gravado no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e16-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="f2e16-110">Os valores padrão são GL \_ verdadeiro, indicando que o componente de cor pode ser escrito.</span><span class="sxs-lookup"><span data-stu-id="f2e16-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="f2e16-111">*amarela*</span><span class="sxs-lookup"><span data-stu-id="f2e16-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e16-112">Especifique se o verde pode ou não ser gravado no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e16-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="f2e16-113">O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.</span><span class="sxs-lookup"><span data-stu-id="f2e16-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="f2e16-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="f2e16-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e16-115">Especifique se azul pode ou não ser gravado no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e16-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="f2e16-116">O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.</span><span class="sxs-lookup"><span data-stu-id="f2e16-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="f2e16-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="f2e16-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e16-118">Especifique se alfa pode ou não ser gravado no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f2e16-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="f2e16-119">O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.</span><span class="sxs-lookup"><span data-stu-id="f2e16-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e16-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2e16-120">Return value</span></span>

<span data-ttu-id="f2e16-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f2e16-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2e16-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f2e16-122">Error codes</span></span>

<span data-ttu-id="f2e16-123">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f2e16-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f2e16-124">Name</span><span class="sxs-lookup"><span data-stu-id="f2e16-124">Name</span></span>                                                                                                  | <span data-ttu-id="f2e16-125">Significado</span><span class="sxs-lookup"><span data-stu-id="f2e16-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2e16-126"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2e16-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f2e16-127">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f2e16-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f2e16-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2e16-128">Remarks</span></span>

<span data-ttu-id="f2e16-129">A função **glColorMask** especifica se os componentes de cor individuais no framebuffer podem ou não ser gravados.</span><span class="sxs-lookup"><span data-stu-id="f2e16-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="f2e16-130">Se *vermelho* é GL \_ falso, por exemplo, nenhuma alteração é feita no componente vermelho de qualquer pixel em qualquer um dos buffers de cor, independentemente da tentativa de operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="f2e16-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="f2e16-131">As alterações em bits individuais de componentes não podem ser controladas.</span><span class="sxs-lookup"><span data-stu-id="f2e16-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="f2e16-132">Em vez disso, as alterações são habilitadas ou desabilitadas para componentes inteiros de cor.</span><span class="sxs-lookup"><span data-stu-id="f2e16-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="f2e16-133">As funções a seguir recuperam informações relacionadas ao **glColorMask**:</span><span class="sxs-lookup"><span data-stu-id="f2e16-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="f2e16-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a cor do argumento GL \_ \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="f2e16-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="f2e16-135">**glGet** com o modo do Argument GL \_ RGBA \_</span><span class="sxs-lookup"><span data-stu-id="f2e16-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e16-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e16-136">Requirements</span></span>



| <span data-ttu-id="f2e16-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e16-137">Requirement</span></span> | <span data-ttu-id="f2e16-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f2e16-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e16-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2e16-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e16-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2e16-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2e16-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2e16-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e16-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2e16-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2e16-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f2e16-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e16-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e16-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f2e16-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2e16-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2e16-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2e16-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2e16-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e16-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e16-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e16-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e16-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2e16-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e16-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f2e16-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f2e16-151">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f2e16-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f2e16-152">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="f2e16-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="f2e16-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f2e16-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f2e16-154">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f2e16-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f2e16-155">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f2e16-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f2e16-156">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="f2e16-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="f2e16-157">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="f2e16-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





