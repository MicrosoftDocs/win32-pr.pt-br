---
title: função glColor3dv (GL. h)
description: Define a cor atual de uma matriz de valores de cor já existente. | função glColor3dv (GL. h)
ms.assetid: 68325214-9218-44de-bbe3-28d8bddab5b5
keywords:
- função glColor3dv OpenGL
topic_type:
- apiref
api_name:
- glColor3dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1874f029d143d91b3ac5ccb9ba95d70e5606a7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930503"
---
# <a name="glcolor3dv-function"></a><span data-ttu-id="5de3d-105">função glColor3dv</span><span class="sxs-lookup"><span data-stu-id="5de3d-105">glColor3dv function</span></span>

<span data-ttu-id="5de3d-106">Define a cor atual de uma matriz de valores de cor já existente.</span><span class="sxs-lookup"><span data-stu-id="5de3d-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de3d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5de3d-107">Syntax</span></span>


```C++
void WINAPI glColor3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="5de3d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5de3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de3d-109">*l*</span><span class="sxs-lookup"><span data-stu-id="5de3d-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5de3d-110">Um ponteiro para uma matriz que contém valores vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="5de3d-110">A pointer to an array that contains red, green, and blue values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de3d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5de3d-111">Return value</span></span>

<span data-ttu-id="5de3d-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5de3d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de3d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5de3d-113">Remarks</span></span>

<span data-ttu-id="5de3d-114">O GL armazena um índice de cor de valor único atual e uma cor RGBA atual de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="5de3d-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="5de3d-115">**glColor** define uma nova cor RGBA de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="5de3d-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="5de3d-116">**glColor** tem duas variantes principais: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="5de3d-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="5de3d-117">as variantes **glcolor3** especificam os novos valores vermelho, verde e azul explicitamente e definem o valor alfa atual como 1,0 (intensidade total) implicitamente.</span><span class="sxs-lookup"><span data-stu-id="5de3d-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="5de3d-118">as variantes de **glcolor4** especificam todos os quatro componentes de cores explicitamente.</span><span class="sxs-lookup"><span data-stu-id="5de3d-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="5de3d-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** levam três ou quatro inteiros de bytes assinados, curtos ou longos como argumentos.</span><span class="sxs-lookup"><span data-stu-id="5de3d-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="5de3d-120">Quando v é anexado ao nome, os comandos Color podem usar um ponteiro para uma matriz desses valores.</span><span class="sxs-lookup"><span data-stu-id="5de3d-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="5de3d-121">Os valores de cor atuais são armazenados no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados.</span><span class="sxs-lookup"><span data-stu-id="5de3d-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="5de3d-122">Os componentes de cor de inteiro não assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante de forma que o maior valor representável seja mapeado para 1,0 (intensidade total) e 0 mapeie para 0,0 (intensidade zero).</span><span class="sxs-lookup"><span data-stu-id="5de3d-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="5de3d-123">Os componentes de cor de inteiro assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="5de3d-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="5de3d-124">(Observe que esse mapeamento não converte 0 precisamente em 0,0.) Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="5de3d-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="5de3d-125">Os valores inteiros de ponto flutuante e inteiro não assinado são clamped para o intervalo de \[ 0, 1 \] antes da atualização da cor atual.</span><span class="sxs-lookup"><span data-stu-id="5de3d-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="5de3d-126">No entanto, os componentes de cor são clamped a esse intervalo antes de serem interpolados ou gravados em um buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="5de3d-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5de3d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5de3d-127">Requirements</span></span>



| <span data-ttu-id="5de3d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de3d-128">Requirement</span></span> | <span data-ttu-id="5de3d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5de3d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5de3d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5de3d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5de3d-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5de3d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5de3d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5de3d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5de3d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5de3d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5de3d-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5de3d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5de3d-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de3d-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5de3d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5de3d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="5de3d-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de3d-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5de3d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5de3d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5de3d-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5de3d-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de3d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5de3d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de3d-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5de3d-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5de3d-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5de3d-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5de3d-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5de3d-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5de3d-144">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5de3d-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





