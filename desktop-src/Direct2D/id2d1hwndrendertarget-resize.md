---
title: Métodos de redimensionamento de ID2D1HwndRenderTarget (D2d1. h)
description: Altera o tamanho do destino de renderização para o tamanho de pixel especificado.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Redimensionar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750922"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="cc436-104">Métodos ID2D1HwndRenderTarget:: Resize</span><span class="sxs-lookup"><span data-stu-id="cc436-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="cc436-105">Altera o tamanho do destino de renderização para o tamanho de pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="cc436-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cc436-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="cc436-106">Overload list</span></span>



| <span data-ttu-id="cc436-107">Método</span><span class="sxs-lookup"><span data-stu-id="cc436-107">Method</span></span>                                                                         | <span data-ttu-id="cc436-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc436-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="cc436-109">[**Redimensionar (D2D1 \_ tamanho \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="cc436-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="cc436-110">Altera o tamanho do destino de renderização para o tamanho de pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="cc436-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="cc436-111">[**Redimensionar ( \_ tamanho de d2d1 \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="cc436-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="cc436-112">Altera o tamanho do destino de renderização para o tamanho de pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="cc436-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="cc436-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc436-113">Remarks</span></span>

<span data-ttu-id="cc436-114">Depois que esse método é chamado, o conteúdo do buffer de fundo do destino de renderização não é definido, mesmo que a opção [**d2d1 \_ apresente as opções de retenção de \_ \_ \_ conteúdo**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) tenha sido especificada quando o destino de renderização foi criado.</span><span class="sxs-lookup"><span data-stu-id="cc436-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc436-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc436-115">Requirements</span></span>



| <span data-ttu-id="cc436-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc436-116">Requirement</span></span> | <span data-ttu-id="cc436-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cc436-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc436-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc436-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc436-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc436-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc436-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc436-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc436-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc436-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc436-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cc436-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc436-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc436-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc436-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc436-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc436-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc436-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="cc436-126">�</span><span class="sxs-lookup"><span data-stu-id="cc436-126">�</span></span>

<span data-ttu-id="cc436-127">�</span><span class="sxs-lookup"><span data-stu-id="cc436-127">�</span></span>
