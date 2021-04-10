---
title: função glIndexfv (GL. h)
description: A função glIndexfv define o índice de cores atual.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- função glIndexfv OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a649f15dd6fad637d9e742a97235fdcd99d82794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009102"
---
# <a name="glindexfv-function"></a><span data-ttu-id="a9a8d-104">função glIndexfv</span><span class="sxs-lookup"><span data-stu-id="a9a8d-104">glIndexfv function</span></span>

<span data-ttu-id="a9a8d-105">A função **glIndexfv** define o índice de cores atual.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-105">The **glIndexfv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a8d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9a8d-106">Syntax</span></span>


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a><span data-ttu-id="a9a8d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9a8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a8d-108">*c*</span><span class="sxs-lookup"><span data-stu-id="a9a8d-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a8d-109">Um ponteiro para uma matriz de um elemento que contém o novo valor para o índice de cores atual.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a8d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9a8d-110">Return value</span></span>

<span data-ttu-id="a9a8d-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a8d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9a8d-112">Remarks</span></span>

<span data-ttu-id="a9a8d-113">A função **glIndexfv** atualiza o índice de cores atual (de valor único).</span><span class="sxs-lookup"><span data-stu-id="a9a8d-113">The **glIndexfv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="a9a8d-114">Ele usa um argumento: o novo valor para o índice de cores atual.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="a9a8d-115">O índice atual é armazenado como um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="a9a8d-116">Os valores inteiros são convertidos diretamente em valores de ponto flutuante, sem mapeamento especial.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="a9a8d-117">Os valores de índice fora do intervalo representável do buffer de índice de cor não são clamped.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="a9a8d-118">No entanto, antes que um índice seja dicedido (se habilitado) e gravado no framebuffer, ele é convertido em formato de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="a9a8d-119">Todos os bits na parte inteira do valor de ponto fixo resultante que não correspondem aos bits no framebuffer são mascarados.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="a9a8d-120">O índice atual pode ser atualizado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a9a8d-120">The current index can be updated at any time.</span></span> <span data-ttu-id="a9a8d-121">Em particular, **glIndexfv** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a9a8d-121">In particular, **glIndexfv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="a9a8d-122">A função a seguir recupera informações relacionadas a **glIndexfv**:</span><span class="sxs-lookup"><span data-stu-id="a9a8d-122">The following function retrieves information related to **glIndexfv**:</span></span>

<span data-ttu-id="a9a8d-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL o \_ \_ índice atual</span><span class="sxs-lookup"><span data-stu-id="a9a8d-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a8d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9a8d-124">Requirements</span></span>



| <span data-ttu-id="a9a8d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a8d-125">Requirement</span></span> | <span data-ttu-id="a9a8d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a9a8d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a8d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a8d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a8d-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9a8d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9a8d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a8d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a8d-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9a8d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9a8d-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9a8d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a8d-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a8d-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a9a8d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9a8d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9a8d-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9a8d-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9a8d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a8d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a8d-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9a8d-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a8d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9a8d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a8d-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a9a8d-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a9a8d-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

