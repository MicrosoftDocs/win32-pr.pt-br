---
title: função gluNurbsCallback (Glu. h)
description: A função gluNurbsCallback define um retorno de chamada para um objeto B-spline racional não uniforme (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- função gluNurbsCallback OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778532"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="09e13-104">função gluNurbsCallback</span><span class="sxs-lookup"><span data-stu-id="09e13-104">gluNurbsCallback function</span></span>

<span data-ttu-id="09e13-105">A função **gluNurbsCallback** define um retorno de chamada para um objeto B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="09e13-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e13-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09e13-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="09e13-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09e13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e13-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="09e13-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="09e13-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="09e13-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="09e13-110">*Onde*</span><span class="sxs-lookup"><span data-stu-id="09e13-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="09e13-111">O retorno de chamada que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="09e13-111">The callback being defined.</span></span> <span data-ttu-id="09e13-112">O único valor válido é GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="09e13-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="09e13-113">O significado do \_ erro Glu significa que a função Error é chamada quando um erro é encontrado.</span><span class="sxs-lookup"><span data-stu-id="09e13-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="09e13-114">Seu único argumento é do tipo **GLenum** e indica o erro específico que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="09e13-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="09e13-115">Há 37 erros exclusivos para NURBS, denominados GLU \_ NURBS \_ ERROR1 por meio de Glu \_ NURBS \_ ERROR37.</span><span class="sxs-lookup"><span data-stu-id="09e13-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="09e13-116">As cadeias de caracteres que descrevem esses erros podem ser recuperadas com [**gluErrorString**](gluerrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="09e13-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="09e13-117">*fn*</span><span class="sxs-lookup"><span data-stu-id="09e13-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="09e13-118">Um ponteiro para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="09e13-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e13-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09e13-119">Return value</span></span>

<span data-ttu-id="09e13-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="09e13-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e13-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="09e13-121">Remarks</span></span>

<span data-ttu-id="09e13-122">Use **gluNurbsCallback** para definir um retorno de chamada a ser usado por um objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="09e13-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="09e13-123">Se o retorno de chamada especificado já estiver definido, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="09e13-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="09e13-124">Se *FN* for **NULL**, qualquer retorno de chamada existente será apagado.</span><span class="sxs-lookup"><span data-stu-id="09e13-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e13-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e13-125">Requirements</span></span>



| <span data-ttu-id="09e13-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e13-126">Requirement</span></span> | <span data-ttu-id="09e13-127">Valor</span><span class="sxs-lookup"><span data-stu-id="09e13-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09e13-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09e13-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09e13-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="09e13-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09e13-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09e13-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="09e13-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09e13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e13-133"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e13-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="09e13-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09e13-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="09e13-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09e13-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="09e13-136">DLL</span><span class="sxs-lookup"><span data-stu-id="09e13-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e13-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e13-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e13-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e13-139">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="09e13-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="09e13-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="09e13-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





