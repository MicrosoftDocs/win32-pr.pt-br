---
title: função glDepthMask (GL. h)
description: A função glDepthMask habilita ou desabilita a gravação no buffer de profundidade.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- função glDepthMask OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369695"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="726c3-104">função glDepthMask</span><span class="sxs-lookup"><span data-stu-id="726c3-104">glDepthMask function</span></span>

<span data-ttu-id="726c3-105">A função **glDepthMask** habilita ou desabilita a gravação no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="726c3-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="726c3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="726c3-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="726c3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="726c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726c3-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="726c3-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="726c3-109">Especifica se o buffer de profundidade está habilitado para gravação.</span><span class="sxs-lookup"><span data-stu-id="726c3-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="726c3-110">Se o *sinalizador* for zero, a gravação de buffer de profundidade será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="726c3-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="726c3-111">Caso contrário, ele será habilitado.</span><span class="sxs-lookup"><span data-stu-id="726c3-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="726c3-112">Inicialmente, a gravação de buffer de profundidade está habilitada.</span><span class="sxs-lookup"><span data-stu-id="726c3-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726c3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="726c3-113">Return value</span></span>

<span data-ttu-id="726c3-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="726c3-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="726c3-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="726c3-115">Error codes</span></span>

<span data-ttu-id="726c3-116">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="726c3-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="726c3-117">Name</span><span class="sxs-lookup"><span data-stu-id="726c3-117">Name</span></span>                                                                                                  | <span data-ttu-id="726c3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="726c3-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="726c3-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="726c3-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="726c3-120">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="726c3-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="726c3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="726c3-121">Remarks</span></span>

<span data-ttu-id="726c3-122">A função a seguir recupera informações relacionadas a **glDepthMask**:</span><span class="sxs-lookup"><span data-stu-id="726c3-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="726c3-123">**glGet** com profundidade de argumento GL \_ \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="726c3-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="726c3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726c3-124">Requirements</span></span>



| <span data-ttu-id="726c3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="726c3-125">Requirement</span></span> | <span data-ttu-id="726c3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="726c3-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="726c3-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="726c3-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="726c3-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="726c3-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="726c3-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="726c3-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="726c3-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="726c3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="726c3-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="726c3-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="726c3-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="726c3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="726c3-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="726c3-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="726c3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="726c3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="726c3-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726c3-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726c3-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="726c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726c3-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="726c3-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="726c3-139">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="726c3-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="726c3-140">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="726c3-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="726c3-141">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="726c3-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="726c3-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="726c3-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="726c3-143">**glGet**</span><span class="sxs-lookup"><span data-stu-id="726c3-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="726c3-144">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="726c3-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="726c3-145">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="726c3-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





