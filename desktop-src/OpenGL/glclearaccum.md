---
title: função glClearAccum (GL. h)
description: A função glClearAccum especifica os valores claros para o buffer de acumulação.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- função glClearAccum OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085705"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="d2f35-104">função glClearAccum</span><span class="sxs-lookup"><span data-stu-id="d2f35-104">glClearAccum function</span></span>

<span data-ttu-id="d2f35-105">A função **glClearAccum** especifica os valores claros para o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="d2f35-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f35-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2f35-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="d2f35-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2f35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f35-108">*vermelho*</span><span class="sxs-lookup"><span data-stu-id="d2f35-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f35-109">O valor vermelho usado quando o buffer de acumulação é limpo.</span><span class="sxs-lookup"><span data-stu-id="d2f35-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="d2f35-110">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="d2f35-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2f35-111">*amarela*</span><span class="sxs-lookup"><span data-stu-id="d2f35-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f35-112">O valor verde usado quando o buffer de acumulação é limpo.</span><span class="sxs-lookup"><span data-stu-id="d2f35-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="d2f35-113">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="d2f35-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2f35-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="d2f35-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f35-115">O valor azul usado quando o buffer de acumulação é limpo.</span><span class="sxs-lookup"><span data-stu-id="d2f35-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="d2f35-116">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="d2f35-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2f35-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="d2f35-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="d2f35-118">O valor alfa usado quando o buffer de acumulação é limpo.</span><span class="sxs-lookup"><span data-stu-id="d2f35-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="d2f35-119">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="d2f35-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f35-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2f35-120">Return value</span></span>

<span data-ttu-id="d2f35-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2f35-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2f35-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d2f35-122">Error codes</span></span>

<span data-ttu-id="d2f35-123">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f35-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d2f35-124">Nome</span><span class="sxs-lookup"><span data-stu-id="d2f35-124">Name</span></span>                                                                                                  | <span data-ttu-id="d2f35-125">Significado</span><span class="sxs-lookup"><span data-stu-id="d2f35-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2f35-126"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f35-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d2f35-127">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d2f35-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d2f35-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2f35-128">Remarks</span></span>

<span data-ttu-id="d2f35-129">A função **glClearAccum** especifica os valores vermelho, verde, azul e alfa usados pelo [**glClear**](glclear.md) para limpar o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="d2f35-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="d2f35-130">Os valores especificados por **glClearAccum** são clamped para o intervalo \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d2f35-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="d2f35-131">A função a seguir recupera informações relacionadas a **glClearAccum**:</span><span class="sxs-lookup"><span data-stu-id="d2f35-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="d2f35-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_</span><span class="sxs-lookup"><span data-stu-id="d2f35-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f35-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f35-133">Requirements</span></span>



| <span data-ttu-id="d2f35-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f35-134">Requirement</span></span> | <span data-ttu-id="d2f35-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d2f35-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f35-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2f35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f35-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2f35-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d2f35-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2f35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f35-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2f35-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2f35-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d2f35-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2f35-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f35-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d2f35-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2f35-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2f35-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f35-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2f35-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d2f35-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2f35-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f35-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f35-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2f35-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f35-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d2f35-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d2f35-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="d2f35-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="d2f35-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d2f35-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d2f35-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d2f35-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





