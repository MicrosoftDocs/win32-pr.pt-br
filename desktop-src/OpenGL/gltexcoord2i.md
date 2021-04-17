---
title: função glTexCoord2i (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord2i (GL. h)
ms.assetid: 7a5ff9a7-8dcd-47a0-868c-3909e011a592
keywords:
- função glTexCoord2i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa4d710f49d55e8aa0379bfc83f79f877d3cc906
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105762931"
---
# <a name="gltexcoord2i-function"></a><span data-ttu-id="6d37e-105">função glTexCoord2i</span><span class="sxs-lookup"><span data-stu-id="6d37e-105">glTexCoord2i function</span></span>

<span data-ttu-id="6d37e-106">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="6d37e-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d37e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d37e-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2i(
   GLint s,
   GLint t
);
```



## <a name="parameters"></a><span data-ttu-id="6d37e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d37e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d37e-109">*s*</span><span class="sxs-lookup"><span data-stu-id="6d37e-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="6d37e-110">A coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="6d37e-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6d37e-111">*t*</span><span class="sxs-lookup"><span data-stu-id="6d37e-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="6d37e-112">A coordenada de textura t.</span><span class="sxs-lookup"><span data-stu-id="6d37e-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d37e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d37e-113">Return value</span></span>

<span data-ttu-id="6d37e-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6d37e-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d37e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d37e-115">Remarks</span></span>

<span data-ttu-id="6d37e-116">A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono.</span><span class="sxs-lookup"><span data-stu-id="6d37e-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="6d37e-117">A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="6d37e-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="6d37e-118">A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6d37e-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="6d37e-119">Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p).</span><span class="sxs-lookup"><span data-stu-id="6d37e-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="6d37e-120">Você pode atualizar as coordenadas de textura atuais a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="6d37e-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="6d37e-121">Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6d37e-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6d37e-122">A função a seguir recupera informações relacionadas a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="6d37e-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="6d37e-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_</span><span class="sxs-lookup"><span data-stu-id="6d37e-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="6d37e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d37e-124">Requirements</span></span>



| <span data-ttu-id="6d37e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d37e-125">Requirement</span></span> | <span data-ttu-id="6d37e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6d37e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d37e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d37e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d37e-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d37e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d37e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d37e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d37e-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d37e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d37e-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d37e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d37e-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d37e-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d37e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d37e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d37e-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d37e-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d37e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6d37e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d37e-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d37e-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d37e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d37e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d37e-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="6d37e-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





