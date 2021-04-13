---
title: função glLoadIdentity (GL. h)
description: A função glLoadIdentity substitui a matriz atual pela matriz de identidade.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- função glLoadIdentity OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568392"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="e0fe1-104">função glLoadIdentity</span><span class="sxs-lookup"><span data-stu-id="e0fe1-104">glLoadIdentity function</span></span>

<span data-ttu-id="e0fe1-105">A função **glLoadIdentity** substitui a matriz atual pela matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fe1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0fe1-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="e0fe1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0fe1-107">Parameters</span></span>

<span data-ttu-id="e0fe1-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0fe1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0fe1-109">Return value</span></span>

<span data-ttu-id="e0fe1-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0fe1-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e0fe1-111">Error codes</span></span>

<span data-ttu-id="e0fe1-112">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e0fe1-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e0fe1-113">Nome</span><span class="sxs-lookup"><span data-stu-id="e0fe1-113">Name</span></span>                                                                                                  | <span data-ttu-id="e0fe1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e0fe1-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0fe1-115"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0fe1-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e0fe1-116">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e0fe1-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e0fe1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0fe1-117">Remarks</span></span>

<span data-ttu-id="e0fe1-118">A função **glLoadIdentity** substitui a matriz atual pela matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="e0fe1-119">É semanticamente equivalente a chamar [**glLoadMatrix**](glloadmatrix.md) com a seguinte matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Diagrama que mostra a matriz de identidade que o glLoadIdentity chama.](images/load01.png)

<span data-ttu-id="e0fe1-121">No entanto, em alguns casos, é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="e0fe1-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="e0fe1-122">As funções a seguir recuperam informações relacionadas ao **glLoadIdentity**:</span><span class="sxs-lookup"><span data-stu-id="e0fe1-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="e0fe1-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="e0fe1-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e0fe1-124">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="e0fe1-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e0fe1-125"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e0fe1-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e0fe1-126">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e0fe1-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fe1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0fe1-127">Requirements</span></span>



| <span data-ttu-id="e0fe1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fe1-128">Requirement</span></span> | <span data-ttu-id="e0fe1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e0fe1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fe1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0fe1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fe1-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0fe1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e0fe1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0fe1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fe1-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0fe1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0fe1-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0fe1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0fe1-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0fe1-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e0fe1-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0fe1-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0fe1-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0fe1-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e0fe1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0fe1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0fe1-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fe1-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fe1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0fe1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fe1-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-143">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-145">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e0fe1-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e0fe1-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





