---
title: função glIndexMask (GL. h)
description: A função glIndexMask controla a gravação de bits individuais nos buffers de índice de cor.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- função glIndexMask OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811312"
---
# <a name="glindexmask-function"></a><span data-ttu-id="2ef09-104">função glIndexMask</span><span class="sxs-lookup"><span data-stu-id="2ef09-104">glIndexMask function</span></span>

<span data-ttu-id="2ef09-105">A função **glIndexMask** controla a gravação de bits individuais nos buffers de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="2ef09-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef09-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ef09-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="2ef09-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ef09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef09-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="2ef09-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef09-109">Uma máscara de bits para habilitar e desabilitar a gravação de bits individuais nos buffers de índice de cores.</span><span class="sxs-lookup"><span data-stu-id="2ef09-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="2ef09-110">Inicialmente, a máscara é tudo.</span><span class="sxs-lookup"><span data-stu-id="2ef09-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef09-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ef09-111">Return value</span></span>

<span data-ttu-id="2ef09-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2ef09-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ef09-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2ef09-113">Error codes</span></span>

<span data-ttu-id="2ef09-114">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef09-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2ef09-115">Nome</span><span class="sxs-lookup"><span data-stu-id="2ef09-115">Name</span></span>                                                                                                  | <span data-ttu-id="2ef09-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2ef09-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ef09-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ef09-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2ef09-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2ef09-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ef09-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef09-119">Remarks</span></span>

<span data-ttu-id="2ef09-120">A função **glIndexMask** controla a gravação de bits individuais nos buffers de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="2ef09-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="2ef09-121">Os *n* bits menos significativos de *Mask*, em que *1* é o número de bits em um buffer de índice de cor, especifique uma máscara.</span><span class="sxs-lookup"><span data-stu-id="2ef09-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="2ef09-122">Sempre que um deles aparecer na máscara, o bit correspondente no buffer de índice de cor (ou buffers) se tornará gravável.</span><span class="sxs-lookup"><span data-stu-id="2ef09-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="2ef09-123">Onde um zero é exibido, o bit é protegido contra gravação.</span><span class="sxs-lookup"><span data-stu-id="2ef09-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="2ef09-124">Essa máscara é usada somente no modo de índice de cor e afeta somente os buffers selecionados atualmente para gravação (consulte [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="2ef09-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="2ef09-125">Inicialmente, todos os bits estão habilitados para gravação.</span><span class="sxs-lookup"><span data-stu-id="2ef09-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="2ef09-126">A função a seguir recupera informações relacionadas a **glIndexMask**:</span><span class="sxs-lookup"><span data-stu-id="2ef09-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="2ef09-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ index \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="2ef09-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef09-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef09-128">Requirements</span></span>



| <span data-ttu-id="2ef09-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef09-129">Requirement</span></span> | <span data-ttu-id="2ef09-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef09-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef09-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef09-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef09-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ef09-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ef09-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef09-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef09-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ef09-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ef09-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ef09-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ef09-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef09-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2ef09-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ef09-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ef09-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ef09-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ef09-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2ef09-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ef09-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ef09-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef09-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ef09-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef09-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2ef09-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2ef09-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="2ef09-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="2ef09-144">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ef09-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="2ef09-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2ef09-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2ef09-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="2ef09-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="2ef09-147">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="2ef09-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





