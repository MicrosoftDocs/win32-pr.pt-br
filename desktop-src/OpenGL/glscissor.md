---
title: função glScissor (GL. h)
description: A função glScissor define a caixa de tesoura.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- função glScissor OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455951"
---
# <a name="glscissor-function"></a><span data-ttu-id="a58a0-104">função glScissor</span><span class="sxs-lookup"><span data-stu-id="a58a0-104">glScissor function</span></span>

<span data-ttu-id="a58a0-105">A função **glScissor** define a caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58a0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a58a0-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="a58a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a58a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a58a0-108">*x*</span><span class="sxs-lookup"><span data-stu-id="a58a0-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a58a0-109">A coordenada x (eixo vertical) para o canto inferior esquerdo da caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="a58a0-110">*y*</span><span class="sxs-lookup"><span data-stu-id="a58a0-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a58a0-111">A coordenada y (eixo horizontal) para o canto inferior esquerdo da caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="a58a0-112">Juntos, x e y especificam o canto inferior esquerdo da caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="a58a0-113">Inicialmente (0, 0).</span><span class="sxs-lookup"><span data-stu-id="a58a0-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="a58a0-114">*width*</span><span class="sxs-lookup"><span data-stu-id="a58a0-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a58a0-115">A largura da caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="a58a0-116">*altura*</span><span class="sxs-lookup"><span data-stu-id="a58a0-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a58a0-117">A altura da caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="a58a0-117">The height of the scissor box.</span></span> <span data-ttu-id="a58a0-118">Quando um contexto OpenGL é anexado *pela primeira vez* a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.</span><span class="sxs-lookup"><span data-stu-id="a58a0-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a58a0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a58a0-119">Return value</span></span>

<span data-ttu-id="a58a0-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a58a0-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a58a0-121">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a58a0-121">Error codes</span></span>

<span data-ttu-id="a58a0-122">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a58a0-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a58a0-123">Nome</span><span class="sxs-lookup"><span data-stu-id="a58a0-123">Name</span></span>                                                                                                  | <span data-ttu-id="a58a0-124">Significado</span><span class="sxs-lookup"><span data-stu-id="a58a0-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a58a0-125"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a58a0-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a58a0-126">A *largura* ou a *altura* era negativa.</span><span class="sxs-lookup"><span data-stu-id="a58a0-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="a58a0-127"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a58a0-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a58a0-128">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a58a0-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a58a0-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a58a0-129">Remarks</span></span>

<span data-ttu-id="a58a0-130">A função **glScissor** define um retângulo, chamado de caixa de tesoura, em coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="a58a0-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="a58a0-131">Os dois primeiros parâmetros, *x* e *y*, especificam o canto inferior esquerdo da caixa.</span><span class="sxs-lookup"><span data-stu-id="a58a0-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="a58a0-132">Os parâmetros *Width* e *Height* especificam a largura e a altura da caixa.</span><span class="sxs-lookup"><span data-stu-id="a58a0-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="a58a0-133">O teste de recorte está habilitado e desabilitado usando [**glEnable**](glenable.md) e **glDisable** com o teste de recorte do Argument GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a58a0-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="a58a0-134">Enquanto o teste de tesoura está habilitado, somente os pixels que estão na caixa de recorte podem ser modificados por comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="a58a0-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="a58a0-135">As coordenadas da janela têm valores inteiros nos cantos compartilhados de framebuffer pixels, portanto, **glScissor**(0, 0, 1, 1) permite que apenas o pixel inferior esquerdo na janela seja modificado e **glScissor**(0, 0, 0, 0) não permita a modificação em todos os pixels na janela.</span><span class="sxs-lookup"><span data-stu-id="a58a0-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="a58a0-136">Quando o teste de tesoura é desabilitado, é como se a caixa de corte incluir a janela inteira.</span><span class="sxs-lookup"><span data-stu-id="a58a0-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="a58a0-137">As funções a seguir recuperam informações relacionadas ao **glScissor**:</span><span class="sxs-lookup"><span data-stu-id="a58a0-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="a58a0-138">caixa de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL de \_ mola \_</span><span class="sxs-lookup"><span data-stu-id="a58a0-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="a58a0-139">teste de recorte de [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a58a0-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="a58a0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a58a0-140">Requirements</span></span>



| <span data-ttu-id="a58a0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a58a0-141">Requirement</span></span> | <span data-ttu-id="a58a0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a58a0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a58a0-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a58a0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a58a0-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a58a0-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a58a0-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a58a0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a58a0-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a58a0-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a58a0-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a58a0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a58a0-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a58a0-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a58a0-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a58a0-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="a58a0-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a58a0-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a58a0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a58a0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a58a0-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a58a0-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a58a0-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="a58a0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58a0-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a58a0-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a58a0-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="a58a0-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="a58a0-156">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a58a0-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a58a0-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a58a0-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="a58a0-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="a58a0-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





