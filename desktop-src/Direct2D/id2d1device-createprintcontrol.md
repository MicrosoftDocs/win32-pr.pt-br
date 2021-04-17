---
title: Métodos ID2D1Device CreatePrintControl (D2d1 \_ 1. h)
description: Cria um objeto ID2D1PrintControl que converte primitivos Direct2D armazenados em ID2D1CommandList em uma representação de página fixa. Em seguida, o subsistema de impressão consome os primitivos.
ms.assetid: C8860AEE-807A-435E-9F44-B50545320EDA
keywords:
- Métodos CreatePrintControl Direct2D
topic_type:
- apiref
api_location:
- d2d1_1.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ec8705d73f40fc967b3247aaf81caebcade47b02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782276"
---
# <a name="id2d1devicecreateprintcontrol-methods"></a><span data-ttu-id="09164-105">Métodos ID2D1Device:: CreatePrintControl</span><span class="sxs-lookup"><span data-stu-id="09164-105">ID2D1Device::CreatePrintControl methods</span></span>

<span data-ttu-id="09164-106">Cria um objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que converte primitivos [Direct2D](/windows/desktop/direct2d/direct2d-portal) armazenados em [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) em uma representação de página fixa.</span><span class="sxs-lookup"><span data-stu-id="09164-106">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="09164-107">Em seguida, o subsistema de impressão consome os primitivos.</span><span class="sxs-lookup"><span data-stu-id="09164-107">The print sub-system then consumes the primitives.</span></span>

### <a name="overload-list"></a><span data-ttu-id="09164-108">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="09164-108">Overload list</span></span>



| <span data-ttu-id="09164-109">Método</span><span class="sxs-lookup"><span data-stu-id="09164-109">Method</span></span>                                                                                                                                                                           | <span data-ttu-id="09164-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09164-110">Description</span></span>                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09164-111">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , d2d1 \_ \_ \_ Propriedades de controle \* de impressão, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="09164-111">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES\*, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span></span> | <span data-ttu-id="09164-112">Cria um objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que converte primitivos [Direct2D](/windows/desktop/direct2d/direct2d-portal) armazenados em [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) em uma representação de página fixa.</span><span class="sxs-lookup"><span data-stu-id="09164-112">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="09164-113">Em seguida, o subsistema de impressão consome os primitivos.</span><span class="sxs-lookup"><span data-stu-id="09164-113">The print sub-system then consumes the primitives.</span></span><br/> |
| <span data-ttu-id="09164-114">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , d2d1 \_ \_ Propriedades de controle \_ de impressão&, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="09164-114">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES&, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span></span>    | <span data-ttu-id="09164-115">Cria um objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que converte primitivos [Direct2D](/windows/desktop/direct2d/direct2d-portal) armazenados em [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) em uma representação de página fixa.</span><span class="sxs-lookup"><span data-stu-id="09164-115">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="09164-116">Em seguida, o subsistema de impressão consome os primitivos.</span><span class="sxs-lookup"><span data-stu-id="09164-116">The print sub-system then consumes the primitives.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="09164-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09164-117">Requirements</span></span>



| <span data-ttu-id="09164-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09164-118">Requirement</span></span> | <span data-ttu-id="09164-119">Valor</span><span class="sxs-lookup"><span data-stu-id="09164-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09164-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09164-120">Header</span></span><br/> | <dl> <span data-ttu-id="09164-121"><dt>D2d1 \_ 1. h</dt></span><span class="sxs-lookup"><span data-stu-id="09164-121"><dt>D2d1\_1.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09164-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="09164-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09164-123">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="09164-123">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
</dt> </dl>

<span data-ttu-id="09164-124">�</span><span class="sxs-lookup"><span data-stu-id="09164-124">�</span></span>

<span data-ttu-id="09164-125">�</span><span class="sxs-lookup"><span data-stu-id="09164-125">�</span></span>
