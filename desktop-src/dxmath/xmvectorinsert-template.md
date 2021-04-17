---
description: Gira um vetor à esquerda por um determinado número de componentes de 32 bits e insere os elementos selecionados desse resultado em outro vetor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modelo XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748655"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="aeb7b-103">Modelo XMVectorInsert</span><span class="sxs-lookup"><span data-stu-id="aeb7b-103">XMVectorInsert template</span></span>

<span data-ttu-id="aeb7b-104">Gira um vetor à esquerda por um determinado número de componentes de 32 bits e insere os elementos selecionados desse resultado em outro vetor.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aeb7b-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="aeb7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeb7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb7b-107"><span id="VD"></span><span id="vd"></span>*VD*</span><span class="sxs-lookup"><span data-stu-id="aeb7b-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="aeb7b-108">\[em \] vetor para inserir.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="aeb7b-109"><span id="VS"></span><span id="vs"></span>*VS*</span><span class="sxs-lookup"><span data-stu-id="aeb7b-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="aeb7b-110">\[em \] vetor para girar para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb7b-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="aeb7b-111">Return Value</span></span>

<span data-ttu-id="aeb7b-112">Retorna o [**XMVECTOR**](xmvector-data-type.md) que resulta da rotação e da inserção.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb7b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeb7b-113">Remarks</span></span>

<span data-ttu-id="aeb7b-114">Essa função é uma versão de modelo do [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , em que os argumentos *Select \** são valores de modelo.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="aeb7b-115">Para obter o melhor desempenho, o resultado de `XMVectorInsert` deve ser atribuído de volta para o *VD*.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="aeb7b-116">O `XMVectorInsert` modelo é novo para DirectXMath e não está disponível para o XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="aeb7b-117">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="aeb7b-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="aeb7b-118">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="aeb7b-118">Platform Requirements</span></span>

<span data-ttu-id="aeb7b-119">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="aeb7b-120">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="aeb7b-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb7b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb7b-121">Requirements</span></span>



| <span data-ttu-id="aeb7b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb7b-122">Requirement</span></span> | <span data-ttu-id="aeb7b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb7b-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb7b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aeb7b-124">Header</span></span><br/> | <dl> <span data-ttu-id="aeb7b-125"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb7b-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb7b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeb7b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb7b-127">Funções de modelo de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="aeb7b-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="aeb7b-128">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="aeb7b-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="aeb7b-129">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="aeb7b-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="aeb7b-130">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="aeb7b-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="aeb7b-131">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="aeb7b-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
