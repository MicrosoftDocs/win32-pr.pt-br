---
title: função glTexCoord3d (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord3d (GL. h)
ms.assetid: 41b8aa69-c069-493f-a1e3-51cf6a01209e
keywords:
- função glTexCoord3d OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb7603ed0f823e3b8d841328378d9e207638716
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506424"
---
# <a name="gltexcoord3d-function"></a><span data-ttu-id="a0bed-105">função glTexCoord3d</span><span class="sxs-lookup"><span data-stu-id="a0bed-105">glTexCoord3d function</span></span>

<span data-ttu-id="a0bed-106">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="a0bed-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0bed-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3d(
   GLdouble s,
   GLdouble t,
   GLdouble r
);
```



## <a name="parameters"></a><span data-ttu-id="a0bed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0bed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0bed-109">*s*</span><span class="sxs-lookup"><span data-stu-id="a0bed-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bed-110">A coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="a0bed-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a0bed-111">*t*</span><span class="sxs-lookup"><span data-stu-id="a0bed-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bed-112">A coordenada de textura t.</span><span class="sxs-lookup"><span data-stu-id="a0bed-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a0bed-113">*r*</span><span class="sxs-lookup"><span data-stu-id="a0bed-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bed-114">A coordenada de textura de r.</span><span class="sxs-lookup"><span data-stu-id="a0bed-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0bed-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0bed-115">Return value</span></span>

<span data-ttu-id="a0bed-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a0bed-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0bed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0bed-117">Remarks</span></span>

<span data-ttu-id="a0bed-118">A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono.</span><span class="sxs-lookup"><span data-stu-id="a0bed-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="a0bed-119">A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="a0bed-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="a0bed-120">A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a0bed-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="a0bed-121">Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p).</span><span class="sxs-lookup"><span data-stu-id="a0bed-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="a0bed-122">Você pode atualizar as coordenadas de textura atuais a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a0bed-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="a0bed-123">Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a0bed-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="a0bed-124">A função a seguir recupera informações relacionadas a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="a0bed-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="a0bed-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_</span><span class="sxs-lookup"><span data-stu-id="a0bed-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bed-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0bed-126">Requirements</span></span>



| <span data-ttu-id="a0bed-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bed-127">Requirement</span></span> | <span data-ttu-id="a0bed-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a0bed-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bed-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0bed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bed-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0bed-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a0bed-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0bed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bed-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0bed-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0bed-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0bed-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0bed-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0bed-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a0bed-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0bed-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0bed-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0bed-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0bed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a0bed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0bed-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0bed-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bed-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0bed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bed-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="a0bed-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





