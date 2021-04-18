---
title: função glEdgeFlag (GL. h)
description: Sinaliza bordas como limite ou não associado. | função glEdgeFlag (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- função glEdgeFlag OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105770465"
---
# <a name="gledgeflag-function"></a><span data-ttu-id="75b41-105">função glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="75b41-105">glEdgeFlag function</span></span>

<span data-ttu-id="75b41-106">Sinaliza bordas como limite ou não associado.</span><span class="sxs-lookup"><span data-stu-id="75b41-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b41-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="75b41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75b41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b41-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="75b41-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="75b41-110">Especifica o valor do sinalizador de borda atual, **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="75b41-110">Specifies the current edge flag value, either **TRUE** or **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b41-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75b41-111">Return value</span></span>

<span data-ttu-id="75b41-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="75b41-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b41-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="75b41-113">Remarks</span></span>

<span data-ttu-id="75b41-114">Cada vértice de um polígono, um triângulo separado ou um diamante separado especificado entre um par [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) é marcado como o início de um limite ou de uma borda não-bound.</span><span class="sxs-lookup"><span data-stu-id="75b41-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="75b41-115">Se o sinalizador de borda atual for **true** quando o vértice for especificado, o vértice será marcado como o início de uma borda de limite.</span><span class="sxs-lookup"><span data-stu-id="75b41-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="75b41-116">Se o sinalizador de borda atual for **false**, o vértice será marcado como o início de uma borda não bound.</span><span class="sxs-lookup"><span data-stu-id="75b41-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="75b41-117">A função **glEdgeFlag** define o sinalizador de borda como **true** se o sinalizador for diferente de zero; caso contrário, **retornará false** .</span><span class="sxs-lookup"><span data-stu-id="75b41-117">The **glEdgeFlag** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="75b41-118">Os vértices dos triângulos conectados e quadrilaterals conectados sempre são marcados como limite, independentemente do valor do sinalizador de borda.</span><span class="sxs-lookup"><span data-stu-id="75b41-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="75b41-119">Os sinalizadores de borda e limites não restritos nos vértices são significativos somente se o \_ \_ modo de polígono GL estiver definido como o \_ ponto GL ou a \_ linha GL.</span><span class="sxs-lookup"><span data-stu-id="75b41-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="75b41-120">Consulte [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="75b41-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="75b41-121">Inicialmente, o bit do sinalizador de borda é **true**.</span><span class="sxs-lookup"><span data-stu-id="75b41-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="75b41-122">O sinalizador de borda atual pode ser atualizado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="75b41-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="75b41-123">Em particular, **glEdgeFlag** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="75b41-123">In particular, **glEdgeFlag** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="75b41-124">As funções a seguir recuperam informações relacionadas ao **glEdgeFlag**:</span><span class="sxs-lookup"><span data-stu-id="75b41-124">The following functions retrieve information related to **glEdgeFlag**:</span></span>

<span data-ttu-id="75b41-125">sinalizador de borda [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="75b41-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="75b41-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b41-126">Requirements</span></span>



| <span data-ttu-id="75b41-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b41-127">Requirement</span></span> | <span data-ttu-id="75b41-128">Valor</span><span class="sxs-lookup"><span data-stu-id="75b41-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b41-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b41-129">Minimum supported client</span></span><br/> | <span data-ttu-id="75b41-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="75b41-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="75b41-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b41-131">Minimum supported server</span></span><br/> | <span data-ttu-id="75b41-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="75b41-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75b41-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75b41-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b41-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b41-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="75b41-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75b41-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="75b41-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75b41-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="75b41-137">DLL</span><span class="sxs-lookup"><span data-stu-id="75b41-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b41-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b41-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

