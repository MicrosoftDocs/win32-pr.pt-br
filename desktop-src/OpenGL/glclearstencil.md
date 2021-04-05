---
title: função glClearStencil (GL. h)
description: A função glClearStencil especifica o valor de limpeza para o buffer de estêncil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- função glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918585"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="9b908-104">função glClearStencil</span><span class="sxs-lookup"><span data-stu-id="9b908-104">glClearStencil function</span></span>

<span data-ttu-id="9b908-105">A função **glClearStencil** especifica o valor de limpeza para o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9b908-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b908-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b908-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="9b908-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b908-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b908-108">*s*</span><span class="sxs-lookup"><span data-stu-id="9b908-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="9b908-109">O índice usado quando o buffer do estêncil é limpo.</span><span class="sxs-lookup"><span data-stu-id="9b908-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="9b908-110">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="9b908-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b908-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b908-111">Return value</span></span>

<span data-ttu-id="9b908-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9b908-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b908-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9b908-113">Error codes</span></span>

<span data-ttu-id="9b908-114">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9b908-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9b908-115">Nome</span><span class="sxs-lookup"><span data-stu-id="9b908-115">Name</span></span>                                                                                                  | <span data-ttu-id="9b908-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9b908-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b908-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9b908-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9b908-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9b908-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b908-119">Remarks</span></span>

<span data-ttu-id="9b908-120">A função **glClearStencil** especifica o índice usado pelo [**glClear**](glclear.md) para limpar o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9b908-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="9b908-121">O parâmetro *s* é mascarado com 2 <sup>m</sup>  -1, em que *m* é o número de bits no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="9b908-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="9b908-122">As funções a seguir recuperam informações relacionadas à função **glClearStencil** :</span><span class="sxs-lookup"><span data-stu-id="9b908-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="9b908-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ valor de \_ limpeza do estêncil GL do argumento \_</span><span class="sxs-lookup"><span data-stu-id="9b908-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="9b908-124">**glGet** com bits de estêncil do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="9b908-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="9b908-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b908-125">Requirements</span></span>



| <span data-ttu-id="9b908-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b908-126">Requirement</span></span> | <span data-ttu-id="9b908-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9b908-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b908-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b908-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b908-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b908-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9b908-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b908-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b908-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b908-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b908-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9b908-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b908-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9b908-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b908-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b908-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b908-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9b908-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b908-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b908-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b908-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b908-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9b908-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9b908-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="9b908-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="9b908-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9b908-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9b908-142">**glGet**</span><span class="sxs-lookup"><span data-stu-id="9b908-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





