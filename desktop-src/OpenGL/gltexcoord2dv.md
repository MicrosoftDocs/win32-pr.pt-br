---
title: função glTexCoord2dv (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord2dv (GL. h)
ms.assetid: e324a5ac-6251-42f8-9483-3d6ad8ae321f
keywords:
- função glTexCoord2dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee3f9269b4a65c7dcef143506b336c0936209ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754974"
---
# <a name="gltexcoord2dv-function"></a><span data-ttu-id="5a5a2-105">função glTexCoord2dv</span><span class="sxs-lookup"><span data-stu-id="5a5a2-105">glTexCoord2dv function</span></span>

<span data-ttu-id="5a5a2-106">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a5a2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a5a2-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="5a5a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a5a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a5a2-109">*l*</span><span class="sxs-lookup"><span data-stu-id="5a5a2-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5a5a2-110">Um ponteiro para uma matriz de dois elementos que, por sua vez, especifica as coordenadas de textura s e t.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-110">A pointer to an array of two elements, which in turn specifies the s and t texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a5a2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a5a2-111">Return value</span></span>

<span data-ttu-id="5a5a2-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a5a2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a5a2-113">Remarks</span></span>

<span data-ttu-id="5a5a2-114">A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="5a5a2-115">A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="5a5a2-116">A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="5a5a2-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="5a5a2-117">Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p).</span><span class="sxs-lookup"><span data-stu-id="5a5a2-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="5a5a2-118">Você pode atualizar as coordenadas de textura atuais a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="5a5a2-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="5a5a2-119">Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5a5a2-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="5a5a2-120">A função a seguir recupera informações relacionadas a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="5a5a2-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="5a5a2-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_</span><span class="sxs-lookup"><span data-stu-id="5a5a2-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="5a5a2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a5a2-122">Requirements</span></span>



| <span data-ttu-id="5a5a2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a5a2-123">Requirement</span></span> | <span data-ttu-id="5a5a2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5a5a2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5a2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a5a2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a5a2-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a5a2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5a5a2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a5a2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a5a2-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a5a2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a5a2-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a5a2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a5a2-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a5a2-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5a5a2-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a5a2-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a5a2-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a5a2-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a5a2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a5a2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a5a2-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a5a2-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a5a2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a5a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a5a2-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="5a5a2-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





