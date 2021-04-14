---
description: Especifique os níveis de proteção para o sistema de gerenciamento de geração de cópia&\# 8212; Analógico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-um sinalizador de proteção (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370544"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="eacee-103">CGMS-um sinalizador de proteção</span><span class="sxs-lookup"><span data-stu-id="eacee-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="eacee-104">As constantes na tabela a seguir especificam os níveis de proteção para o sistema de gerenciamento de geração de cópia analógica (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="eacee-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="eacee-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="eacee-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="eacee-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="eacee-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="eacee-107"><dt>**OPM \_ CGMSA \_ off**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="eacee-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="eacee-108">CGMS-A está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="eacee-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="eacee-109"><dt>**OPM \_ CGMSA de \_ cópia \_ gratuita**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eacee-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="eacee-110">O nível de proteção é cópia livre.</span><span class="sxs-lookup"><span data-stu-id="eacee-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="eacee-111"><dt>**OPM \_ CGMSA \_ copiar \_ não \_ mais**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="eacee-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="eacee-112">O nível de proteção não é mais.</span><span class="sxs-lookup"><span data-stu-id="eacee-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="eacee-113"><dt>**OPM \_ CGMSA \_ copiar \_ uma \_**</dt> <dt>0x03</dt> de geração</span><span class="sxs-lookup"><span data-stu-id="eacee-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="eacee-114">O nível de proteção é cópia de uma geração.</span><span class="sxs-lookup"><span data-stu-id="eacee-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="eacee-115"><dt>**OPM \_ \_Cópia CGMSA \_ nunca**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="eacee-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="eacee-116">O nível de proteção nunca é cópia.</span><span class="sxs-lookup"><span data-stu-id="eacee-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="eacee-117"><dt>**OPM \_ \_Controle de redistribuição CGMSA \_ \_ necessário**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="eacee-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="eacee-118">É necessário o controle de redistribuição (também chamado de *sinalizador de difusão*).</span><span class="sxs-lookup"><span data-stu-id="eacee-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="eacee-119">Esse sinalizador pode ser combinado com os outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="eacee-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eacee-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="eacee-120">Remarks</span></span>

<span data-ttu-id="eacee-121">Esses sinalizadores são equivalentes às constantes de enumeração de **\_ nível de \_ proteção \_ Copp CGMSA** usadas no protocolo Copp (certificado de proteção de saída).</span><span class="sxs-lookup"><span data-stu-id="eacee-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="eacee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eacee-122">Requirements</span></span>



| <span data-ttu-id="eacee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eacee-123">Requirement</span></span> | <span data-ttu-id="eacee-124">Valor</span><span class="sxs-lookup"><span data-stu-id="eacee-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eacee-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eacee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eacee-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eacee-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eacee-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eacee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eacee-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eacee-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eacee-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eacee-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eacee-130"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eacee-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eacee-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="eacee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eacee-132">Media Foundation constantes</span><span class="sxs-lookup"><span data-stu-id="eacee-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




