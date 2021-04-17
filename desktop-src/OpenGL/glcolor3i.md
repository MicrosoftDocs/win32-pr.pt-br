---
title: função glColor3i (GL. h)
description: Define a cor atual. | função glColor3i (GL. h)
ms.assetid: 9c68221b-1633-435b-9ae4-abc1c52601aa
keywords:
- função glColor3i OpenGL
topic_type:
- apiref
api_name:
- glColor3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bb94421d44f7aed14c793c0f95d7b6467d7e38
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105758448"
---
# <a name="glcolor3i-function"></a><span data-ttu-id="7cee3-105">função glColor3i</span><span class="sxs-lookup"><span data-stu-id="7cee3-105">glColor3i function</span></span>

<span data-ttu-id="7cee3-106">Define a cor atual.</span><span class="sxs-lookup"><span data-stu-id="7cee3-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cee3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cee3-107">Syntax</span></span>


```C++
void WINAPI glColor3i(
   GLint red,
   GLint green,
   GLint blue
);
```



## <a name="parameters"></a><span data-ttu-id="7cee3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cee3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cee3-109">*vermelho*</span><span class="sxs-lookup"><span data-stu-id="7cee3-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="7cee3-110">O novo valor vermelho para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="7cee3-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="7cee3-111">*amarela*</span><span class="sxs-lookup"><span data-stu-id="7cee3-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="7cee3-112">O novo valor verde para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="7cee3-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="7cee3-113">*azul*</span><span class="sxs-lookup"><span data-stu-id="7cee3-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="7cee3-114">O novo valor azul para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="7cee3-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cee3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cee3-115">Return value</span></span>

<span data-ttu-id="7cee3-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7cee3-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cee3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cee3-117">Remarks</span></span>

<span data-ttu-id="7cee3-118">O GL armazena um índice de cor de valor único atual e uma cor RGBA atual de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="7cee3-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="7cee3-119">**glColor** define uma nova cor RGBA de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="7cee3-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="7cee3-120">**glColor** tem duas variantes principais: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="7cee3-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="7cee3-121">as variantes **glcolor3** especificam os novos valores vermelho, verde e azul explicitamente e definem o valor alfa atual como 1,0 (intensidade total) implicitamente.</span><span class="sxs-lookup"><span data-stu-id="7cee3-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="7cee3-122">as variantes de **glcolor4** especificam todos os quatro componentes de cores explicitamente.</span><span class="sxs-lookup"><span data-stu-id="7cee3-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="7cee3-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** levam três ou quatro inteiros de bytes assinados, curtos ou longos como argumentos.</span><span class="sxs-lookup"><span data-stu-id="7cee3-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="7cee3-124">Quando v é anexado ao nome, os comandos Color podem usar um ponteiro para uma matriz desses valores.</span><span class="sxs-lookup"><span data-stu-id="7cee3-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="7cee3-125">Os valores de cor atuais são armazenados no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados.</span><span class="sxs-lookup"><span data-stu-id="7cee3-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="7cee3-126">Os componentes de cor de inteiro não assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante de forma que o maior valor representável seja mapeado para 1,0 (intensidade total) e 0 mapeie para 0,0 (intensidade zero).</span><span class="sxs-lookup"><span data-stu-id="7cee3-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="7cee3-127">Os componentes de cor de inteiro assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="7cee3-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7cee3-128">(Observe que esse mapeamento não converte 0 precisamente em 0,0.) Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="7cee3-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="7cee3-129">Os valores inteiros de ponto flutuante e inteiro não assinado são clamped para o intervalo de \[ 0, 1 \] antes da atualização da cor atual.</span><span class="sxs-lookup"><span data-stu-id="7cee3-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="7cee3-130">No entanto, os componentes de cor são clamped a esse intervalo antes de serem interpolados ou gravados em um buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="7cee3-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cee3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cee3-131">Requirements</span></span>



| <span data-ttu-id="7cee3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cee3-132">Requirement</span></span> | <span data-ttu-id="7cee3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7cee3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cee3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cee3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7cee3-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cee3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7cee3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cee3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7cee3-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cee3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cee3-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7cee3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cee3-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cee3-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7cee3-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cee3-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cee3-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cee3-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cee3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7cee3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cee3-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cee3-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cee3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cee3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cee3-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7cee3-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7cee3-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7cee3-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7cee3-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7cee3-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7cee3-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="7cee3-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





