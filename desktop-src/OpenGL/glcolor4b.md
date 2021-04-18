---
title: função glColor4b (GL. h)
description: Define a cor atual. | função glColor4b (GL. h)
ms.assetid: 50d829f2-f336-40be-8598-a255c86f0722
keywords:
- função glColor4b OpenGL
topic_type:
- apiref
api_name:
- glColor4b
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd16d3bb752b5e640e86636929de9d8706ab49a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755336"
---
# <a name="glcolor4b-function"></a><span data-ttu-id="540f7-105">função glColor4b</span><span class="sxs-lookup"><span data-stu-id="540f7-105">glColor4b function</span></span>

<span data-ttu-id="540f7-106">Define a cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="540f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="540f7-107">Syntax</span></span>


```C++
void WINAPI glColor4b(
   GLbyte red,
   GLbyte green,
   GLbyte blue,
   GLbyte alpha
);
```



## <a name="parameters"></a><span data-ttu-id="540f7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="540f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="540f7-109">*vermelho*</span><span class="sxs-lookup"><span data-stu-id="540f7-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="540f7-110">O novo valor vermelho para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="540f7-111">*amarela*</span><span class="sxs-lookup"><span data-stu-id="540f7-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="540f7-112">O novo valor verde para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="540f7-113">*azul*</span><span class="sxs-lookup"><span data-stu-id="540f7-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="540f7-114">O novo valor azul para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-114">The new blue value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="540f7-115">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="540f7-115">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="540f7-116">O novo valor alfa para a cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-116">The new alpha value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="540f7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="540f7-117">Return value</span></span>

<span data-ttu-id="540f7-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="540f7-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="540f7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="540f7-119">Remarks</span></span>

<span data-ttu-id="540f7-120">O GL armazena um índice de cor de valor único atual e uma cor RGBA atual de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="540f7-120">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="540f7-121">**glColor** define uma nova cor RGBA de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="540f7-121">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="540f7-122">**glColor** tem duas variantes principais: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="540f7-122">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="540f7-123">as variantes **glcolor3** especificam os novos valores vermelho, verde e azul explicitamente e definem o valor alfa atual como 1,0 (intensidade total) implicitamente.</span><span class="sxs-lookup"><span data-stu-id="540f7-123">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="540f7-124">as variantes de **glcolor4** especificam todos os quatro componentes de cores explicitamente.</span><span class="sxs-lookup"><span data-stu-id="540f7-124">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="540f7-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** levam três ou quatro inteiros de bytes assinados, curtos ou longos como argumentos.</span><span class="sxs-lookup"><span data-stu-id="540f7-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="540f7-126">Quando v é anexado ao nome, os comandos Color podem usar um ponteiro para uma matriz desses valores.</span><span class="sxs-lookup"><span data-stu-id="540f7-126">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="540f7-127">Os valores de cor atuais são armazenados no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados.</span><span class="sxs-lookup"><span data-stu-id="540f7-127">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="540f7-128">Os componentes de cor de inteiro não assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante de forma que o maior valor representável seja mapeado para 1,0 (intensidade total) e 0 mapeie para 0,0 (intensidade zero).</span><span class="sxs-lookup"><span data-stu-id="540f7-128">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="540f7-129">Os componentes de cor de inteiro assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="540f7-129">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="540f7-130">(Observe que esse mapeamento não converte 0 precisamente em 0,0.) Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="540f7-130">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="540f7-131">Os valores inteiros de ponto flutuante e inteiro não assinado são clamped para o intervalo de \[ 0, 1 \] antes da atualização da cor atual.</span><span class="sxs-lookup"><span data-stu-id="540f7-131">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="540f7-132">No entanto, os componentes de cor são clamped a esse intervalo antes de serem interpolados ou gravados em um buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="540f7-132">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="540f7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="540f7-133">Requirements</span></span>



| <span data-ttu-id="540f7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="540f7-134">Requirement</span></span> | <span data-ttu-id="540f7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="540f7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="540f7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="540f7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="540f7-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="540f7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="540f7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="540f7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="540f7-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="540f7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="540f7-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="540f7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="540f7-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="540f7-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="540f7-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="540f7-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="540f7-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="540f7-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="540f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="540f7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="540f7-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="540f7-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="540f7-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="540f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540f7-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="540f7-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="540f7-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="540f7-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="540f7-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="540f7-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="540f7-150">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="540f7-150">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





