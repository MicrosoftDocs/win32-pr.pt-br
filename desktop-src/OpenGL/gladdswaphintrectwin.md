---
title: função glAddSwapHintRectWIN (GL. h)
description: A função de retorno de chamada glAddSwapHintRectWIN especifica um conjunto de retângulos que devem ser copiados pelo SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- função glAddSwapHintRectWIN OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369703"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="3991a-104">função glAddSwapHintRectWIN</span><span class="sxs-lookup"><span data-stu-id="3991a-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="3991a-105">A função de retorno de chamada **glAddSwapHintRectWIN** especifica um conjunto de retângulos que devem ser copiados pelo [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="3991a-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="3991a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3991a-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="3991a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3991a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3991a-108">*x*</span><span class="sxs-lookup"><span data-stu-id="3991a-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="3991a-109">A coordenada *x*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.</span><span class="sxs-lookup"><span data-stu-id="3991a-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-110">*y*</span><span class="sxs-lookup"><span data-stu-id="3991a-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="3991a-111">A coordenada *y*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.</span><span class="sxs-lookup"><span data-stu-id="3991a-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-112">*width*</span><span class="sxs-lookup"><span data-stu-id="3991a-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="3991a-113">A largura do retângulo da região de dica.</span><span class="sxs-lookup"><span data-stu-id="3991a-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3991a-114">*altura*</span><span class="sxs-lookup"><span data-stu-id="3991a-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="3991a-115">A altura do retângulo da região de dica.</span><span class="sxs-lookup"><span data-stu-id="3991a-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3991a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3991a-116">Return value</span></span>

<span data-ttu-id="3991a-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3991a-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3991a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3991a-118">Remarks</span></span>

<span data-ttu-id="3991a-119">A função **glAddSwapHintRectWIN** acelera a animação, reduzindo a quantidade de repintura entre quadros.</span><span class="sxs-lookup"><span data-stu-id="3991a-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="3991a-120">Com o **glAddSwapHintRectWIN**, você especifica um conjunto de áreas retangulares que deseja copiar ao chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="3991a-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="3991a-121">Quando você não especificar retângulos com **glAddSwapHintRectWIN** antes de chamar **SwapBuffers**, a framebuffer inteira será trocada.</span><span class="sxs-lookup"><span data-stu-id="3991a-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="3991a-122">O uso de **glAddSwapHintRectWIN** para copiar apenas partes alteradas do buffer pode aumentar significativamente o desempenho do **SwapBuffers**, especialmente quando o **SwapBuffers** é implementado no software.</span><span class="sxs-lookup"><span data-stu-id="3991a-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="3991a-123">A função **glAddSwapHintRectWIN** adiciona um retângulo à região de dica.</span><span class="sxs-lookup"><span data-stu-id="3991a-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="3991a-124">Quando o \_ \_ sinalizador de cópia de permuta PFD da estrutura de formato [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel é definido, **SwapBuffers** usa essa região para recortar a cópia do buffer de fundo para o buffer frontal.</span><span class="sxs-lookup"><span data-stu-id="3991a-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="3991a-125">Você não especifica \_ \_ a cópia de permuta PFD; ela é definida pelo hardware compatível.</span><span class="sxs-lookup"><span data-stu-id="3991a-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="3991a-126">A região de dica é desmarcada após cada chamada para **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="3991a-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="3991a-127">Com algumas configurações de hardware, o **SwapBuffers** pode ignorar a região de dicas e trocar o buffer inteiro.</span><span class="sxs-lookup"><span data-stu-id="3991a-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="3991a-128">O **SwapBuffers** é implementado pelo sistema, não pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3991a-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="3991a-129">O OpenGL mantém uma região de dica separada para cada janela.</span><span class="sxs-lookup"><span data-stu-id="3991a-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="3991a-130">Quando você chama **glAddSwapHintRectWIN** em quaisquer contextos de renderização associados a uma janela, os retângulos de dica são combinados em uma única região.</span><span class="sxs-lookup"><span data-stu-id="3991a-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="3991a-131">Chame **glAddSwapHintRectWIN** com um retângulo delimitador para cada objeto desenhado para um quadro e para cada retângulo limpo para apagar objetos de quadro anteriores.</span><span class="sxs-lookup"><span data-stu-id="3991a-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="3991a-132">A função **glAddSwapHintRectWIN** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da \_ extensão de dica GL Win \_ swap \_ .</span><span class="sxs-lookup"><span data-stu-id="3991a-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="3991a-133">Para verificar se a implementação do OpenGL dá suporte a **glAddSwapHintRectWIN**, chame **glGetString**( \_ extensões GL).</span><span class="sxs-lookup"><span data-stu-id="3991a-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="3991a-134">Se retornar a \_ dica GL Win \_ swap \_ , **glAddSwapHintRectWIN** terá suporte.</span><span class="sxs-lookup"><span data-stu-id="3991a-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="3991a-135">Para obter o endereço de uma função de extensão, chame **wglGetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="3991a-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3991a-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3991a-136">Requirements</span></span>



| <span data-ttu-id="3991a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3991a-137">Requirement</span></span> | <span data-ttu-id="3991a-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3991a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3991a-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3991a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3991a-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3991a-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="3991a-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3991a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3991a-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3991a-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3991a-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3991a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3991a-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3991a-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3991a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="3991a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3991a-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="3991a-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="3991a-147">**PIXELFORMATDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="3991a-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="3991a-148">**SwapBuffers**</span><span class="sxs-lookup"><span data-stu-id="3991a-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="3991a-149">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="3991a-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





