---
title: Constantes de WINBIO_ORIENTATION (WinBio \_ Types. h)
description: As constantes a seguir especificam as possíveis orientações de câmera que o componente de sensor especifica como obrigatório.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824813"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="6b870-103">Constantes de orientação de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="6b870-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="6b870-104">As constantes a seguir especificam as possíveis orientações de câmera que o componente de sensor especifica como obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6b870-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="6b870-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6b870-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="6b870-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b870-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="6b870-107"><dt>**WINBIO \_ ORIENTAÇÃO \_ não especificada**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b870-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="6b870-108">Não foi especificada uma orientação obrigatória para a câmera.</span><span class="sxs-lookup"><span data-stu-id="6b870-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="6b870-109"><dt>**WINBIO \_ \_Paisagem de orientação**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6b870-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="6b870-110">A orientação paisagem é necessária para a câmera.</span><span class="sxs-lookup"><span data-stu-id="6b870-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="6b870-111"><dt>**WINBIO \_ ORIENTAÇÃO \_ retrato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6b870-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="6b870-112">A orientação retrato é necessária para a câmera.</span><span class="sxs-lookup"><span data-stu-id="6b870-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="6b870-113"><dt>**WINBIO \_ ORIENTAÇÃO de \_ qualquer**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6b870-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="6b870-114">Qualquer orientação é permitida para a câmera.</span><span class="sxs-lookup"><span data-stu-id="6b870-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="6b870-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b870-115">Requirements</span></span>



| <span data-ttu-id="6b870-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b870-116">Requirement</span></span> | <span data-ttu-id="6b870-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6b870-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b870-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b870-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b870-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6b870-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="6b870-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b870-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b870-121">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="6b870-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="6b870-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b870-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b870-123"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="6b870-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b870-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b870-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b870-125">**\_informações do \_ sensor ESTENDIdo WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="6b870-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





