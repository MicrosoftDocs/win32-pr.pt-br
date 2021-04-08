---
title: função glStencilMask (GL. h)
description: A função glStencilMask controla a gravação de bits individuais nos planos de estêncil.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- função glStencilMask OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086462"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="683e0-104">função glStencilMask</span><span class="sxs-lookup"><span data-stu-id="683e0-104">glStencilMask function</span></span>

<span data-ttu-id="683e0-105">A função **glStencilMask** controla a gravação de bits individuais nos planos de estêncil.</span><span class="sxs-lookup"><span data-stu-id="683e0-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="683e0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683e0-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="683e0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683e0-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="683e0-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="683e0-109">Uma máscara de bits para habilitar e desabilitar a gravação de bits individuais nos planos de estêncil.</span><span class="sxs-lookup"><span data-stu-id="683e0-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="683e0-110">Inicialmente, a máscara é tudo.</span><span class="sxs-lookup"><span data-stu-id="683e0-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="683e0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="683e0-111">Return value</span></span>

<span data-ttu-id="683e0-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="683e0-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="683e0-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="683e0-113">Error codes</span></span>

<span data-ttu-id="683e0-114">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="683e0-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="683e0-115">Nome</span><span class="sxs-lookup"><span data-stu-id="683e0-115">Name</span></span>                                                                                                  | <span data-ttu-id="683e0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="683e0-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="683e0-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="683e0-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="683e0-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="683e0-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="683e0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="683e0-119">Remarks</span></span>

<span data-ttu-id="683e0-120">A função **glStencilMask** controla a gravação de bits individuais nos planos de estêncil.</span><span class="sxs-lookup"><span data-stu-id="683e0-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="683e0-121">Os *n* bits menos significativos de *Mask*, em que *n* é o número de bits no buffer do estêncil, especifique uma máscara.</span><span class="sxs-lookup"><span data-stu-id="683e0-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="683e0-122">Sempre que um deles aparecer na máscara, o bit correspondente no buffer do estêncil será gravável.</span><span class="sxs-lookup"><span data-stu-id="683e0-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="683e0-123">Onde um zero é exibido, o bit é protegido contra gravação.</span><span class="sxs-lookup"><span data-stu-id="683e0-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="683e0-124">Inicialmente, todos os bits estão habilitados para gravação.</span><span class="sxs-lookup"><span data-stu-id="683e0-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="683e0-125">As funções a seguir recuperam informações relacionadas ao **glStencilMask**:</span><span class="sxs-lookup"><span data-stu-id="683e0-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="683e0-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ WRITEMASK de estêncil do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="683e0-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="683e0-127">glGet com bits de estêncil do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="683e0-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="683e0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683e0-128">Requirements</span></span>



| <span data-ttu-id="683e0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="683e0-129">Requirement</span></span> | <span data-ttu-id="683e0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="683e0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="683e0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683e0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="683e0-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="683e0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="683e0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683e0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="683e0-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="683e0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="683e0-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="683e0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="683e0-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="683e0-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="683e0-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="683e0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="683e0-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="683e0-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="683e0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="683e0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683e0-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683e0-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683e0-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="683e0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683e0-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="683e0-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="683e0-143">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="683e0-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="683e0-144">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="683e0-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="683e0-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="683e0-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="683e0-146">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="683e0-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="683e0-147">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="683e0-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="683e0-148">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="683e0-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





