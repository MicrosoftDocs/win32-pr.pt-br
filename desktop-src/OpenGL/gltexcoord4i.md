---
title: função glTexCoord4i (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord4i (GL. h)
ms.assetid: b2b49102-5129-49cc-9043-22ba46fbf08f
keywords:
- função glTexCoord4i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ecdcddc7a62a2cce4adf595321c72dd877aa69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105768696"
---
# <a name="gltexcoord4i-function"></a><span data-ttu-id="a113c-105">função glTexCoord4i</span><span class="sxs-lookup"><span data-stu-id="a113c-105">glTexCoord4i function</span></span>

<span data-ttu-id="a113c-106">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="a113c-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a113c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a113c-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4i(
   GLint s,
   GLint t,
   GLint r,
   GLint q
);
```



## <a name="parameters"></a><span data-ttu-id="a113c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a113c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a113c-109">*s*</span><span class="sxs-lookup"><span data-stu-id="a113c-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="a113c-110">A coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="a113c-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a113c-111">*t*</span><span class="sxs-lookup"><span data-stu-id="a113c-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="a113c-112">A coordenada de textura t.</span><span class="sxs-lookup"><span data-stu-id="a113c-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a113c-113">*r*</span><span class="sxs-lookup"><span data-stu-id="a113c-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="a113c-114">A coordenada de textura de r.</span><span class="sxs-lookup"><span data-stu-id="a113c-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a113c-115">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="a113c-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="a113c-116">A coordenada de textura q.</span><span class="sxs-lookup"><span data-stu-id="a113c-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a113c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a113c-117">Return value</span></span>

<span data-ttu-id="a113c-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a113c-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a113c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a113c-119">Remarks</span></span>

<span data-ttu-id="a113c-120">A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono.</span><span class="sxs-lookup"><span data-stu-id="a113c-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="a113c-121">A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="a113c-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="a113c-122">A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a113c-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="a113c-123">Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p).</span><span class="sxs-lookup"><span data-stu-id="a113c-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="a113c-124">Você pode atualizar as coordenadas de textura atuais a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a113c-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="a113c-125">Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a113c-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="a113c-126">A função a seguir recupera informações relacionadas a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="a113c-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="a113c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_</span><span class="sxs-lookup"><span data-stu-id="a113c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="a113c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a113c-128">Requirements</span></span>



| <span data-ttu-id="a113c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a113c-129">Requirement</span></span> | <span data-ttu-id="a113c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a113c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a113c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a113c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a113c-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a113c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a113c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a113c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a113c-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a113c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a113c-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a113c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a113c-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a113c-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a113c-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a113c-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a113c-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a113c-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a113c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a113c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a113c-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a113c-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a113c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a113c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a113c-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="a113c-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





