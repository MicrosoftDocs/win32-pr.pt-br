---
title: função glEdgeFlagv (GL. h)
description: Sinaliza bordas como limite ou não associado. | função glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- função glEdgeFlagv OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298283"
---
# <a name="gledgeflagv-function"></a><span data-ttu-id="ba47d-105">função glEdgeFlagv</span><span class="sxs-lookup"><span data-stu-id="ba47d-105">glEdgeFlagv function</span></span>

<span data-ttu-id="ba47d-106">Sinaliza bordas como limite ou não associado.</span><span class="sxs-lookup"><span data-stu-id="ba47d-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba47d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba47d-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a><span data-ttu-id="ba47d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba47d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba47d-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="ba47d-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="ba47d-110">Especifica um ponteiro para uma matriz que contém um único elemento booliano, que substitui o valor do sinalizador de borda atual.</span><span class="sxs-lookup"><span data-stu-id="ba47d-110">Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba47d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba47d-111">Return value</span></span>

<span data-ttu-id="ba47d-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ba47d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba47d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba47d-113">Remarks</span></span>

<span data-ttu-id="ba47d-114">Cada vértice de um polígono, um triângulo separado ou um diamante separado especificado entre um par [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) é marcado como o início de um limite ou de uma borda não-bound.</span><span class="sxs-lookup"><span data-stu-id="ba47d-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="ba47d-115">Se o sinalizador de borda atual for **true** quando o vértice for especificado, o vértice será marcado como o início de uma borda de limite.</span><span class="sxs-lookup"><span data-stu-id="ba47d-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="ba47d-116">Se o sinalizador de borda atual for **false**, o vértice será marcado como o início de uma borda não bound.</span><span class="sxs-lookup"><span data-stu-id="ba47d-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="ba47d-117">A função **glEdgeFlagv** define o sinalizador de borda como **true** se o sinalizador for diferente de zero; caso contrário, **retornará false** .</span><span class="sxs-lookup"><span data-stu-id="ba47d-117">The **glEdgeFlagv** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="ba47d-118">Os vértices dos triângulos conectados e quadrilaterals conectados sempre são marcados como limite, independentemente do valor do sinalizador de borda.</span><span class="sxs-lookup"><span data-stu-id="ba47d-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="ba47d-119">Os sinalizadores de borda e limites não restritos nos vértices são significativos somente se o \_ \_ modo de polígono GL estiver definido como o \_ ponto GL ou a \_ linha GL.</span><span class="sxs-lookup"><span data-stu-id="ba47d-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="ba47d-120">Consulte [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="ba47d-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="ba47d-121">Inicialmente, o bit do sinalizador de borda é **true**.</span><span class="sxs-lookup"><span data-stu-id="ba47d-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="ba47d-122">O sinalizador de borda atual pode ser atualizado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="ba47d-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="ba47d-123">Em particular, **glEdgeFlagv** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="ba47d-123">In particular, **glEdgeFlagv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="ba47d-124">As funções a seguir recuperam informações relacionadas ao **glEdgeFlagv**:</span><span class="sxs-lookup"><span data-stu-id="ba47d-124">The following functions retrieve information related to **glEdgeFlagv**:</span></span>

<span data-ttu-id="ba47d-125">sinalizador de borda [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba47d-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="ba47d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba47d-126">Requirements</span></span>



| <span data-ttu-id="ba47d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba47d-127">Requirement</span></span> | <span data-ttu-id="ba47d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ba47d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba47d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba47d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba47d-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba47d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ba47d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba47d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba47d-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba47d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba47d-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba47d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba47d-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba47d-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ba47d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba47d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba47d-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba47d-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba47d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ba47d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba47d-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba47d-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

