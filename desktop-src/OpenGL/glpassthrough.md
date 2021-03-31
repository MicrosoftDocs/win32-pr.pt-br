---
title: função glPassThrough (GL. h)
description: A função glPassThrough coloca um marcador no buffer de comentários.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- função glPassThrough OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644558"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="58a2c-104">função glPassThrough</span><span class="sxs-lookup"><span data-stu-id="58a2c-104">glPassThrough function</span></span>

<span data-ttu-id="58a2c-105">A função **glPassThrough** coloca um marcador no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="58a2c-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a2c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58a2c-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="58a2c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58a2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a2c-108">*token*</span><span class="sxs-lookup"><span data-stu-id="58a2c-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="58a2c-109">Um valor de marcador a ser colocado no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="58a2c-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="58a2c-110">Ele é indicado com o seguinte valor de identificação exclusivo.</span><span class="sxs-lookup"><span data-stu-id="58a2c-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="58a2c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="58a2c-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="58a2c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="58a2c-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="58a2c-113"><dt>**\_token de passagem GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58a2c-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="58a2c-114">A ordem dos comandos **glPassThrough** em relação à especificação de primitivos gráficos é mantida.</span><span class="sxs-lookup"><span data-stu-id="58a2c-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a2c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58a2c-115">Return value</span></span>

<span data-ttu-id="58a2c-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="58a2c-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58a2c-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="58a2c-117">Error codes</span></span>

<span data-ttu-id="58a2c-118">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="58a2c-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="58a2c-119">Name</span><span class="sxs-lookup"><span data-stu-id="58a2c-119">Name</span></span>                                                                                                  | <span data-ttu-id="58a2c-120">Significado</span><span class="sxs-lookup"><span data-stu-id="58a2c-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58a2c-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58a2c-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="58a2c-122">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="58a2c-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="58a2c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="58a2c-123">Remarks</span></span>

<span data-ttu-id="58a2c-124">Feedback é um modo de renderização OpenGL selecionado chamando [**glRenderMode**](glrendermode.md) com os \_ comentários GL.</span><span class="sxs-lookup"><span data-stu-id="58a2c-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="58a2c-125">Quando OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização.</span><span class="sxs-lookup"><span data-stu-id="58a2c-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="58a2c-126">Em vez disso, as informações sobre primitivas que teriam sido rasterizadas são alimentadas de volta para o aplicativo por OpenGL.</span><span class="sxs-lookup"><span data-stu-id="58a2c-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="58a2c-127">Consulte [**glFeedbackBuffer**](glfeedbackbuffer.md) para obter uma descrição do buffer de comentários e os valores contidos nele.</span><span class="sxs-lookup"><span data-stu-id="58a2c-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="58a2c-128">A função **glPassThrough** insere um marcador definido pelo usuário no buffer de comentários quando ele é executado no modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="58a2c-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="58a2c-129">O parâmetro de *token* é retornado como se fosse um primitivo.</span><span class="sxs-lookup"><span data-stu-id="58a2c-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="58a2c-130">A função **glPassThrough** será ignorada se OpenGL não estiver no modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="58a2c-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="58a2c-131">A função a seguir recupera informações relacionadas a **glPassThrough**:</span><span class="sxs-lookup"><span data-stu-id="58a2c-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="58a2c-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="58a2c-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="58a2c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58a2c-133">Requirements</span></span>



| <span data-ttu-id="58a2c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="58a2c-134">Requirement</span></span> | <span data-ttu-id="58a2c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="58a2c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58a2c-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58a2c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="58a2c-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58a2c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58a2c-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58a2c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="58a2c-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58a2c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58a2c-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58a2c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a2c-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="58a2c-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="58a2c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58a2c-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="58a2c-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58a2c-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58a2c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="58a2c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58a2c-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a2c-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a2c-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="58a2c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a2c-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="58a2c-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="58a2c-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="58a2c-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="58a2c-149">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="58a2c-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="58a2c-150">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="58a2c-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





