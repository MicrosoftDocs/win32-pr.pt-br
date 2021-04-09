---
title: Método ID2D1CommandSink1 SetPrimitiveBlend1
description: Define um novo modo de mesclagem primitiva.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Método SetPrimitiveBlend1 Direct2D
- Método SetPrimitiveBlend1 Direct2D, interface ID2D1CommandSink1
- ID2D1CommandSink1 interface Direct2D, método SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085496"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="d19a6-106">Método ID2D1CommandSink1:: SetPrimitiveBlend1</span><span class="sxs-lookup"><span data-stu-id="d19a6-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="d19a6-107">Define um novo modo de mesclagem primitiva.</span><span class="sxs-lookup"><span data-stu-id="d19a6-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19a6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d19a6-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="d19a6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d19a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19a6-110">*primitiveBlend*</span><span class="sxs-lookup"><span data-stu-id="d19a6-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="d19a6-111">Tipo: **[ **d2d1 \_ PRIMITIVE \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="d19a6-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="d19a6-112">A mistura primitiva que será aplicada aos primitivos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d19a6-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19a6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d19a6-113">Return value</span></span>

<span data-ttu-id="d19a6-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d19a6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d19a6-115">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d19a6-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d19a6-116">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d19a6-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d19a6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d19a6-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="d19a6-118">Modos do Blend</span><span class="sxs-lookup"><span data-stu-id="d19a6-118">Blend modes</span></span>

<span data-ttu-id="d19a6-119">Para a renderização com alias (exceto para o modo MIN), o valor de saída O é calculado por meio da interpolação linear do valor *Blend (S, D)* com o valor de pixel de destino, com base no valor que o primitivo cobre o pixel de destino.</span><span class="sxs-lookup"><span data-stu-id="d19a6-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="d19a6-120">A tabela aqui mostra os modos de mistura primitivos para mesclagem com alias e suavização de alias.</span><span class="sxs-lookup"><span data-stu-id="d19a6-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="d19a6-121">As equações listadas na tabela usam estes elementos:</span><span class="sxs-lookup"><span data-stu-id="d19a6-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="d19a6-122">O = saída</span><span class="sxs-lookup"><span data-stu-id="d19a6-122">O = Output</span></span>
-   <span data-ttu-id="d19a6-123">S = origem</span><span class="sxs-lookup"><span data-stu-id="d19a6-123">S = Source</span></span>
-   <span data-ttu-id="d19a6-124">SA = origem alfa</span><span class="sxs-lookup"><span data-stu-id="d19a6-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="d19a6-125">D = destino</span><span class="sxs-lookup"><span data-stu-id="d19a6-125">D = Destination</span></span>
-   <span data-ttu-id="d19a6-126">DA = destino alfa</span><span class="sxs-lookup"><span data-stu-id="d19a6-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="d19a6-127">C = cobertura de pixel</span><span class="sxs-lookup"><span data-stu-id="d19a6-127">C = Pixel coverage</span></span>



| <span data-ttu-id="d19a6-128">Modo de mesclagem primitiva</span><span class="sxs-lookup"><span data-stu-id="d19a6-128">Primitive blend mode</span></span>                 | <span data-ttu-id="d19a6-129">Mesclagem com alias</span><span class="sxs-lookup"><span data-stu-id="d19a6-129">Aliased blending</span></span>                            | <span data-ttu-id="d19a6-130">Mesclagem AntiAlias</span><span class="sxs-lookup"><span data-stu-id="d19a6-130">Antialiased blending</span></span>            | <span data-ttu-id="d19a6-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d19a6-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d19a6-132">\_Origem de \_ mesclagem primitiva \_ de d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="d19a6-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="d19a6-133">O = (S + (1 SA) \* D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="d19a6-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="d19a6-134">O = S \* C + D \* (1 SA \* c)</span><span class="sxs-lookup"><span data-stu-id="d19a6-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="d19a6-135">O modo de mesclagem de origem por destino padrão.</span><span class="sxs-lookup"><span data-stu-id="d19a6-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="d19a6-136">\_Cópia de \_ mistura \_ primitiva de d2d1</span><span class="sxs-lookup"><span data-stu-id="d19a6-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="d19a6-137">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="d19a6-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="d19a6-138">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="d19a6-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="d19a6-139">A origem é copiada para o destino; os pixels de destino são ignorados.</span><span class="sxs-lookup"><span data-stu-id="d19a6-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="d19a6-140">D2D1 \_ PRIMITIVE \_ Blend \_ min</span><span class="sxs-lookup"><span data-stu-id="d19a6-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="d19a6-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="d19a6-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="d19a6-142">O = min (S \* c + 1 SA \* c, D)</span><span class="sxs-lookup"><span data-stu-id="d19a6-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="d19a6-143">Os valores de pixel resultantes usam o mínimo dos valores de pixel de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="d19a6-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="d19a6-144">Disponível no Windows 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d19a6-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="d19a6-145">\_Adição de \_ mistura \_ primitiva de d2d1</span><span class="sxs-lookup"><span data-stu-id="d19a6-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="d19a6-146">O = (S + D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="d19a6-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="d19a6-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="d19a6-147">O = S \* C + D</span></span>                  | <span data-ttu-id="d19a6-148">Os valores de pixel resultantes são a soma dos valores de pixel de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="d19a6-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="d19a6-149">Disponível no Windows 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d19a6-149">Available in Windows 8 and later.</span></span>     |



 

![uma ilustração dos modos de mesclagem primitiva de Direct2D com opacidade e planos de fundo variados.](images/primblenddemo.png)

<span data-ttu-id="d19a6-151">Uma ilustração dos modos de mistura primitiva com opacidade e planos de fundo variados.</span><span class="sxs-lookup"><span data-stu-id="d19a6-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="d19a6-152">O primitivo Blend será aplicado a todos os primitivos desenhados no contexto, a menos que isso seja substituído pelo parâmetro *compositemode* na API do [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .</span><span class="sxs-lookup"><span data-stu-id="d19a6-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="d19a6-153">O primitivo Blend se aplica ao interior de quaisquer primitivos desenhados no contexto.</span><span class="sxs-lookup"><span data-stu-id="d19a6-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="d19a6-154">No caso do [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), isso será implícito pelo retângulo da imagem, pelo deslocamento e pela transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="d19a6-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="d19a6-155">Se o primitivo Blend for algo diferente de **d2d1 \_ primitiva \_ Blend \_** , a renderização de ClearType será desativada.</span><span class="sxs-lookup"><span data-stu-id="d19a6-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="d19a6-156">Se o aplicativo forçar explicitamente a renderização de ClearType nesses modos, o contexto de desenho será colocado em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="d19a6-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="d19a6-157">\_ \_ O estado incorreto do D2DERR será retornado de [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="d19a6-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="d19a6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d19a6-158">Requirements</span></span>



| <span data-ttu-id="d19a6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="d19a6-159">Requirement</span></span> | <span data-ttu-id="d19a6-160">Valor</span><span class="sxs-lookup"><span data-stu-id="d19a6-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d19a6-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d19a6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d19a6-162">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d19a6-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d19a6-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d19a6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d19a6-164">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d19a6-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d19a6-165">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="d19a6-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d19a6-166">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="d19a6-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d19a6-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="d19a6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19a6-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="d19a6-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

