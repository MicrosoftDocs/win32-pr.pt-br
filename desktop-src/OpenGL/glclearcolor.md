---
title: função glClearColor (GL. h)
description: A função glClearColor especifica valores claros para os buffers de cor.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- função glClearColor OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644759"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="5ebd1-104">função glClearColor</span><span class="sxs-lookup"><span data-stu-id="5ebd1-104">glClearColor function</span></span>

<span data-ttu-id="5ebd1-105">A função **glClearColor** especifica valores claros para os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebd1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ebd1-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="5ebd1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ebd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebd1-108">*vermelho*</span><span class="sxs-lookup"><span data-stu-id="5ebd1-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebd1-109">O valor vermelho que o [**glClear**](glclear.md) usa para limpar os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="5ebd1-110">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd1-111">*amarela*</span><span class="sxs-lookup"><span data-stu-id="5ebd1-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebd1-112">O valor verde que o [**glClear**](glclear.md) usa para limpar os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="5ebd1-113">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd1-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="5ebd1-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebd1-115">O valor azul que o [**glClear**](glclear.md) usa para limpar os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="5ebd1-116">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd1-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="5ebd1-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebd1-118">O valor alfa que o [**glClear**](glclear.md) usa para limpar os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="5ebd1-119">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebd1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ebd1-120">Return value</span></span>

<span data-ttu-id="5ebd1-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ebd1-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5ebd1-122">Error codes</span></span>

<span data-ttu-id="5ebd1-123">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebd1-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5ebd1-124">Nome</span><span class="sxs-lookup"><span data-stu-id="5ebd1-124">Name</span></span>                                                                                                  | <span data-ttu-id="5ebd1-125">Significado</span><span class="sxs-lookup"><span data-stu-id="5ebd1-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ebd1-126"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd1-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5ebd1-127">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5ebd1-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5ebd1-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ebd1-128">Remarks</span></span>

<span data-ttu-id="5ebd1-129">A função **glClearColor** especifica os valores vermelho, verde, azul e alfa usados pelo [**glClear**](glclear.md) para limpar os buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="5ebd1-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="5ebd1-130">Os valores especificados por **glClearColor** são clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5ebd1-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="5ebd1-131">As funções a seguir recuperam informações relacionadas à função **glClearColor** :</span><span class="sxs-lookup"><span data-stu-id="5ebd1-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="5ebd1-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_</span><span class="sxs-lookup"><span data-stu-id="5ebd1-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="5ebd1-133">**glGet** com o \_ valor de \_ limpeza de cor do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="5ebd1-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebd1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebd1-134">Requirements</span></span>



| <span data-ttu-id="5ebd1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebd1-135">Requirement</span></span> | <span data-ttu-id="5ebd1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebd1-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebd1-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebd1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebd1-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ebd1-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5ebd1-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebd1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebd1-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ebd1-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ebd1-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ebd1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebd1-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd1-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5ebd1-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ebd1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ebd1-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd1-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ebd1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebd1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebd1-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd1-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebd1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebd1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebd1-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5ebd1-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5ebd1-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="5ebd1-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="5ebd1-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5ebd1-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5ebd1-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="5ebd1-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





