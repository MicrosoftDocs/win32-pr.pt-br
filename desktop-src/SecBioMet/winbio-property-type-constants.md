---
title: Constantes de WINBIO_PROPERTY_TYPE (WinBio. h)
description: Especifique a origem das informações de propriedade na função WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455991"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="239ea-103">Constantes do tipo de \_ Propriedade WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="239ea-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="239ea-104">As constantes **de \_ \_ tipo de propriedade WINBIO** a seguir podem ser usadas para especificar a origem das informações de propriedade na função [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .</span><span class="sxs-lookup"><span data-stu-id="239ea-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="239ea-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_sessão do \_ tipo de propriedade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="239ea-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="239ea-106">A propriedade se aplica a uma sessão biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="239ea-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="239ea-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_modelo de \_ tipo de propriedade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="239ea-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="239ea-108">A propriedade se aplica a um modelo biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="239ea-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="239ea-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unidade de \_ tipo de propriedade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="239ea-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="239ea-110">A propriedade se aplica a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="239ea-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="239ea-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_conta do \_ tipo de propriedade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="239ea-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="239ea-112">A propriedade se aplica a uma conta de usuário específica que tenha um registro biométrico.</span><span class="sxs-lookup"><span data-stu-id="239ea-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="239ea-113">Esse valor tem suporte a partir do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="239ea-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="239ea-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="239ea-114">Requirements</span></span>



| <span data-ttu-id="239ea-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="239ea-115">Requirement</span></span> | <span data-ttu-id="239ea-116">Valor</span><span class="sxs-lookup"><span data-stu-id="239ea-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239ea-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="239ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="239ea-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="239ea-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="239ea-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="239ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="239ea-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="239ea-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="239ea-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="239ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="239ea-122"><dt>WinBio. h (incluir WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="239ea-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239ea-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="239ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239ea-124">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="239ea-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="239ea-125">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="239ea-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





