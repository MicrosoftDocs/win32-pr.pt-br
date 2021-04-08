---
title: Constantes de WINBIO_SETTING_SOURCE (WinBio \_ Types. h)
description: Determine se o Windows Biometric Framework está habilitado no momento.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919137"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="28f01-103">Constantes de origem da \_ configuração WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="28f01-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="28f01-104">As constantes a seguir são usadas pela função [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) para determinar se o Windows Biometric Framework está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="28f01-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="28f01-105">As constantes especificam onde a configuração foi originada.</span><span class="sxs-lookup"><span data-stu-id="28f01-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="28f01-106">Constante</span><span class="sxs-lookup"><span data-stu-id="28f01-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="28f01-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28f01-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="28f01-108"><dt>**\_origem de configuração WINBIO \_ \_ inválida**</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="28f01-109">A configuração não é válida.</span><span class="sxs-lookup"><span data-stu-id="28f01-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="28f01-110"><dt>**\_padrão de \_ origem de configuração WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="28f01-111">A configuração foi originada da política interna.</span><span class="sxs-lookup"><span data-stu-id="28f01-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="28f01-112"><dt>**\_política de \_ origem de configuração de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="28f01-113">A configuração foi originada no registro do computador local.</span><span class="sxs-lookup"><span data-stu-id="28f01-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="28f01-114"><dt>**configuração de WINBIO \_ \_ local de origem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="28f01-115">A configuração foi criada por Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="28f01-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="28f01-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28f01-116">Requirements</span></span>



| <span data-ttu-id="28f01-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28f01-117">Requirement</span></span> | <span data-ttu-id="28f01-118">Valor</span><span class="sxs-lookup"><span data-stu-id="28f01-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f01-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28f01-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28f01-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="28f01-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="28f01-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28f01-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28f01-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="28f01-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="28f01-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28f01-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f01-124"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f01-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="28f01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f01-126">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="28f01-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





