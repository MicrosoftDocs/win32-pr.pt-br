---
title: Constantes de WINBIO_BIR_PURPOSE (WinBio \_ Types. h)
description: Especifique a finalidade para a qual o registro de informações biométricas (BIR) é pretendido ou para o qual ele é adequado.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918505"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="8d7c6-103">Constantes de finalidade de \_ Bir WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="8d7c6-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="8d7c6-104">Os sinalizadores a seguir são usados pelo membro de **finalidade** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) para especificar a finalidade para a qual o Bir (registro de informações biométricas) é pretendido ou para o qual ele é adequado.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="8d7c6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8d7c6-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="8d7c6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d7c6-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="8d7c6-107"><dt>**WINBIO \_ nenhuma \_ finalidade \_ disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="8d7c6-108">Nenhuma finalidade foi especificada.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="8d7c6-109"><dt>**\_verificação de finalidade do WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="8d7c6-110">Verifique a identidade de um usuário.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="8d7c6-111"><dt>**\_identificação de finalidade do WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="8d7c6-112">Identificar um usuário.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="8d7c6-113"><dt>**\_registro de finalidade do WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="8d7c6-114">Registrar um usuário.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="8d7c6-115"><dt>**\_ \_ registro de finalidade \_ do WINBIO para \_ verificação**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="8d7c6-116">Capture um exemplo biométrico e determine se o exemplo corresponde à identidade de usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="8d7c6-117"><dt>**\_ \_ registro de finalidade \_ do WINBIO para \_ identificação**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="8d7c6-118">Capture um exemplo biométrico e determine se ele corresponde a um modelo biométrico existente.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="8d7c6-119"><dt>**\_auditoria de finalidade do WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="8d7c6-120">Informações extras que podem ser usadas para registro em log ou para exibição.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="8d7c6-121">Esse valor é ignorado na entrada por todas as funções.</span><span class="sxs-lookup"><span data-stu-id="8d7c6-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="8d7c6-122">Na saída, ela só estará disponível se houver suporte da unidade biométrica e você especificar o **\_ sinalizador de dados WINBIO \_ \_ RAW** no parâmetro *flags* da função [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .</span><span class="sxs-lookup"><span data-stu-id="8d7c6-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8d7c6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d7c6-123">Requirements</span></span>



| <span data-ttu-id="8d7c6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d7c6-124">Requirement</span></span> | <span data-ttu-id="8d7c6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8d7c6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7c6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7c6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8d7c6-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8d7c6-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="8d7c6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7c6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8d7c6-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8d7c6-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8d7c6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d7c6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d7c6-131"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c6-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d7c6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d7c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7c6-133">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="8d7c6-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="8d7c6-134">**\_cabeçalho WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="8d7c6-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





