---
title: função glTexCoord1dv (GL. h)
description: Define as coordenadas de textura atuais. | função glTexCoord1dv (GL. h)
ms.assetid: 7e7fa328-8267-4e85-9b0f-d7f23052afe6
keywords:
- função glTexCoord1dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11147d70db78fe6bf9d02e807bbc6eafe8089a52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760036"
---
# <a name="gltexcoord1dv-function"></a><span data-ttu-id="9a689-105">função glTexCoord1dv</span><span class="sxs-lookup"><span data-stu-id="9a689-105">glTexCoord1dv function</span></span>

<span data-ttu-id="9a689-106">Define as coordenadas de textura atuais.</span><span class="sxs-lookup"><span data-stu-id="9a689-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a689-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a689-107">Syntax</span></span>


```C++
void WINAPI glTexCoord1dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="9a689-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a689-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a689-109">*l*</span><span class="sxs-lookup"><span data-stu-id="9a689-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-110">Um ponteiro para uma matriz de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="9a689-110">A pointer to an array of texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a689-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a689-111">Return value</span></span>

<span data-ttu-id="9a689-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9a689-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a689-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a689-113">Remarks</span></span>

<span data-ttu-id="9a689-114">A função [**glTexCoord**](gltexcoord-functions.md) define as coordenadas de textura atuais que fazem parte dos dados associados a vértices de polígono.</span><span class="sxs-lookup"><span data-stu-id="9a689-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="9a689-115">A função **glTexCoord** especifica as coordenadas de textura em uma, duas, três ou quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="9a689-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="9a689-116">A função glTexCoord1 define as coordenadas de textura atuais como (s, 0, 0, 1); uma chamada para glTexCoord2 os define como (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="9a689-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="9a689-117">Da mesma forma, glTexCoord3 especifica as coordenadas de textura como (s, t, r, 1) e glTexCoord4 define todos os quatro componentes explicitamente como (s, t, r, p).</span><span class="sxs-lookup"><span data-stu-id="9a689-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="9a689-118">Você pode atualizar as coordenadas de textura atuais a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="9a689-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="9a689-119">Em particular, você pode chamar glTexCoord entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9a689-120">A função a seguir recupera informações relacionadas a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="9a689-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="9a689-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ CoOrds de textura atual \_</span><span class="sxs-lookup"><span data-stu-id="9a689-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="9a689-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a689-122">Requirements</span></span>



| <span data-ttu-id="9a689-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a689-123">Requirement</span></span> | <span data-ttu-id="9a689-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9a689-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a689-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a689-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a689-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a689-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9a689-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a689-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a689-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a689-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a689-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a689-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a689-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9a689-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a689-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a689-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9a689-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9a689-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a689-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a689-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a689-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a689-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="9a689-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





