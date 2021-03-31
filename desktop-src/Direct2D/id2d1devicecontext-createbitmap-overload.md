---
title: Métodos CreateBitmap ID2D1DeviceContext
description: Cria um bitmap que pode ser usado como uma superfície de destino, para leitura de volta à CPU ou como uma fonte para as APIs DrawBitmap e ID2D1BitmapBrush. Além disso, as informações de contexto de cor podem ser passadas para o bitmap.
ms.assetid: D1896DEE-4464-48D7-8EFB-18E564E1F88D
keywords:
- Métodos CreateBitmap Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 6086aeef2ee36da9bd3b917ffdae07f3eb6312bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641235"
---
# <a name="id2d1devicecontextcreatebitmap-methods"></a><span data-ttu-id="7f75d-105">Métodos ID2D1DeviceContext:: CreateBitmap</span><span class="sxs-lookup"><span data-stu-id="7f75d-105">ID2D1DeviceContext::CreateBitmap methods</span></span>

<span data-ttu-id="7f75d-106">Cria um bitmap que pode ser usado como uma superfície de destino, para leitura de volta à CPU ou como uma fonte para as APIs [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="7f75d-106">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="7f75d-107">Além disso, as informações de contexto de cor podem ser passadas para o bitmap. [**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)) getbitmap</span><span class="sxs-lookup"><span data-stu-id="7f75d-107">In addition, color context information can be passed to the bitmap.[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>

### <a name="overload-list"></a><span data-ttu-id="7f75d-108">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="7f75d-108">Overload list</span></span>



| <span data-ttu-id="7f75d-109">Método</span><span class="sxs-lookup"><span data-stu-id="7f75d-109">Method</span></span>                                                                                                                                 | <span data-ttu-id="7f75d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f75d-110">Description</span></span>                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f75d-111">[**CreateBitmap (D2D1 \_ tamanho \_ U, void \* , UINT32, d2d1 \_ bitmap \_ PROPERTIES1, ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="7f75d-111">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>  | <span data-ttu-id="7f75d-112">Cria um bitmap que pode ser usado como uma superfície de destino, para leitura de volta à CPU ou como uma fonte para as APIs [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="7f75d-112">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="7f75d-113">Além disso, as informações de contexto de cor podem ser passadas para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="7f75d-113">In addition, color context information can be passed to the bitmap.</span></span><br/> |
| <span data-ttu-id="7f75d-114">[**CreateBitmap (D2D1 \_ tamanho \_ U, void \* , UINT32, d2d1 \_ bitmap \_ PROPERTIES1 \* , ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="7f75d-114">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1\*, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7f75d-115">[**CreateBitmap (D2D1 \_ tamanho \_ U, void \* , UINT32, D2D1 \_ bitmap \_ PROPERTIES1&, ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="7f75d-115">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1&, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="7f75d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f75d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f75d-117">**ID2D1DeviceContext**</span><span class="sxs-lookup"><span data-stu-id="7f75d-117">**ID2D1DeviceContext**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)
</dt> </dl>

 

