---
title: Constantes de WINBIO_BIOMETRIC_SENSOR_SUBTYPE (WinBio \_ Types. h)
description: Especifique um bitmask para os recursos do sensor integrado.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369476"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="46cd6-103">\_ \_ Constantes de subtipo de sensor BIOmétrico WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="46cd6-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="46cd6-104">As constantes a seguir podem ser usadas como um bitmask para o parâmetro *Capabilities* da estrutura de [**\_ \_ esquema de unidade WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="46cd6-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="46cd6-105">Eles se referem aos recursos do sensor integrado.</span><span class="sxs-lookup"><span data-stu-id="46cd6-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="46cd6-106">Constante</span><span class="sxs-lookup"><span data-stu-id="46cd6-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="46cd6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46cd6-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="46cd6-108"><dt>**subtipo de \_ sensor WINBIO \_ \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd6-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="46cd6-109">Os subtipos de sensor não são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="46cd6-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="46cd6-110"><dt>**\_deslize o \_ \_ subtipo do \_ sensor de WINBIO FP**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd6-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="46cd6-111">O sensor dá suporte a passes de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="46cd6-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="46cd6-112"><dt>**\_toque de \_ \_ subtipo de \_ sensor de WINBIO FP**</dt></span><span class="sxs-lookup"><span data-stu-id="46cd6-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="46cd6-113">O sensor dá suporte a toques de dedos.</span><span class="sxs-lookup"><span data-stu-id="46cd6-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="46cd6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cd6-114">Requirements</span></span>



| <span data-ttu-id="46cd6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cd6-115">Requirement</span></span> | <span data-ttu-id="46cd6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="46cd6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46cd6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cd6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="46cd6-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="46cd6-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="46cd6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cd6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="46cd6-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="46cd6-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="46cd6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46cd6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="46cd6-122"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46cd6-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cd6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="46cd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cd6-124">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="46cd6-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="46cd6-125">**\_esquema de unidade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="46cd6-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





