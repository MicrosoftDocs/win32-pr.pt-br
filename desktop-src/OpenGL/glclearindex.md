---
title: função glClearIndex (GL. h)
description: A função glClearIndex especifica o valor de limpeza para os buffers de índice de cor.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- função glClearIndex OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455321"
---
# <a name="glclearindex-function"></a><span data-ttu-id="4c3a6-104">função glClearIndex</span><span class="sxs-lookup"><span data-stu-id="4c3a6-104">glClearIndex function</span></span>

<span data-ttu-id="4c3a6-105">A função **glClearIndex** especifica o valor de limpeza para os buffers de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3a6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c3a6-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="4c3a6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c3a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3a6-108">*c*</span><span class="sxs-lookup"><span data-stu-id="4c3a6-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="4c3a6-109">O índice usado quando os buffers de índice de cor são apagados.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="4c3a6-110">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c3a6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c3a6-111">Return value</span></span>

<span data-ttu-id="4c3a6-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c3a6-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4c3a6-113">Error codes</span></span>

<span data-ttu-id="4c3a6-114">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4c3a6-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4c3a6-115">Nome</span><span class="sxs-lookup"><span data-stu-id="4c3a6-115">Name</span></span>                                                                                                  | <span data-ttu-id="4c3a6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4c3a6-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c3a6-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a6-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4c3a6-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a6-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4c3a6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c3a6-119">Remarks</span></span>

<span data-ttu-id="4c3a6-120">A função **glClearIndex** especifica o índice usado pelo [**glClear**](glclear.md) para limpar os buffers de índice de cores.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="4c3a6-121">O parâmetro *c* não é clamped.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="4c3a6-122">Em vez disso, *c* é convertido em um valor de ponto fixo com precisão não especificada à direita do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="4c3a6-123">A parte inteira desse valor é então mascarada com 2 <sup>m</sup>  -1, em que *m* é o número de bits em um índice de cores armazenado no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="4c3a6-124">As funções a seguir recuperam informações relacionadas ao **glClearIndex**:</span><span class="sxs-lookup"><span data-stu-id="4c3a6-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="4c3a6-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ \_ valor Clear do índice do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="4c3a6-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="4c3a6-126">**glGet** com bits de índice do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c3a6-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3a6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3a6-127">Requirements</span></span>



| <span data-ttu-id="4c3a6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3a6-128">Requirement</span></span> | <span data-ttu-id="4c3a6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4c3a6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3a6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3a6-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c3a6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4c3a6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3a6-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c3a6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c3a6-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c3a6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c3a6-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a6-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4c3a6-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c3a6-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c3a6-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a6-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c3a6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4c3a6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c3a6-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c3a6-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3a6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c3a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3a6-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4c3a6-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4c3a6-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="4c3a6-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="4c3a6-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4c3a6-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4c3a6-144">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4c3a6-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





