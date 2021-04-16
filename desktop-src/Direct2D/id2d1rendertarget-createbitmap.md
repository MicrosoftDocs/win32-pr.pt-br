---
title: Métodos CreateBitmap ID2D1RenderTarget
description: Cria um bitmap Direct2D.
ms.assetid: b45d353f-ae33-4110-b7c8-f14661017e0f
keywords:
- Métodos CreateBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4576b9111d9180b395527bad8b06ee3f9a8eef2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782272"
---
# <a name="id2d1rendertargetcreatebitmap-methods"></a><span data-ttu-id="156ab-104">Métodos ID2D1RenderTarget:: CreateBitmap</span><span class="sxs-lookup"><span data-stu-id="156ab-104">ID2D1RenderTarget::CreateBitmap methods</span></span>

<span data-ttu-id="156ab-105">Cria um bitmap Direct2D.</span><span class="sxs-lookup"><span data-stu-id="156ab-105">Creates a Direct2D bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="156ab-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="156ab-106">Overload list</span></span>



| <span data-ttu-id="156ab-107">Método</span><span class="sxs-lookup"><span data-stu-id="156ab-107">Method</span></span>                                                                                                                                                                                                   | <span data-ttu-id="156ab-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="156ab-108">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="156ab-109">[**CreateBitmap (tamanho do D2D1 \_ \_ U, \_ Propriedades de bitmap d2d1 \_&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="156ab-109">[**CreateBitmap(D2D1\_SIZE\_U,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span>                                | <span data-ttu-id="156ab-110">Cria um bitmap Direct2D não inicializado.</span><span class="sxs-lookup"><span data-stu-id="156ab-110">Creates an uninitialized Direct2D bitmap.</span></span> <br/>                          |
| <span data-ttu-id="156ab-111">[**CreateBitmap (tamanho de D2D1 \_ \_ U, void \* , UINT32, \_ \_ Propriedades de bitmap d2d1 \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="156ab-111">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES\*,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span> | <span data-ttu-id="156ab-112">Cria um bitmap Direct2D de um ponteiro para dados de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="156ab-112">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span><br/>  |
| <span data-ttu-id="156ab-113">[**CreateBitmap (tamanho de D2D1 \_ \_ U, void \* , UINT32, \_ \_ Propriedades de bitmap d2d1&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="156ab-113">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span></span>  | <span data-ttu-id="156ab-114">Cria um bitmap Direct2D de um ponteiro para dados de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="156ab-114">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="156ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="156ab-115">Requirements</span></span>



| <span data-ttu-id="156ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="156ab-116">Requirement</span></span> | <span data-ttu-id="156ab-117">Valor</span><span class="sxs-lookup"><span data-stu-id="156ab-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="156ab-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="156ab-118">Library</span></span><br/> | <dl> <span data-ttu-id="156ab-119"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="156ab-119"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="156ab-120">DLL</span><span class="sxs-lookup"><span data-stu-id="156ab-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="156ab-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="156ab-121"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="156ab-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="156ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156ab-123">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="156ab-123">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

