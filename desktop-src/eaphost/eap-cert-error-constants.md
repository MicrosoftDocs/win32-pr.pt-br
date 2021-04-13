---
title: '\_Constantes de erro de certificado EAP (Eaphosterror. h)'
description: Defina erros relacionados a certificados comuns a todas as tecnologias de API do EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499287"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="4f010-103">\_Constantes de erro de certificado EAP</span><span class="sxs-lookup"><span data-stu-id="4f010-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="4f010-104">Essas constantes definem erros relacionados a certificados comuns a todas as tecnologias de API do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="4f010-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="4f010-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificado EAP \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="4f010-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-106">0x0</span><span class="sxs-lookup"><span data-stu-id="4f010-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="4f010-107">Define o limite dos relatórios de erros; ocorrerá qualquer erro de certificado entre o certificado **\_ EAP \_ \_ primeiro** e o **\_ \_ certificado EAP \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="4f010-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_certificado EAP \_ último**</span><span class="sxs-lookup"><span data-stu-id="4f010-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-109">0xF</span><span class="sxs-lookup"><span data-stu-id="4f010-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="4f010-110">Define o limite dos relatórios de erros; ocorrerá qualquer erro de certificado entre o certificado **\_ EAP \_ \_ primeiro** e o **\_ \_ certificado EAP \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="4f010-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificado EAP \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4f010-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-112">0x1</span><span class="sxs-lookup"><span data-stu-id="4f010-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="4f010-113">Nenhum certificado de usuário foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4f010-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificado EAP \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="4f010-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-115">0x2</span><span class="sxs-lookup"><span data-stu-id="4f010-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="4f010-116">O certificado de usuário é inválido.</span><span class="sxs-lookup"><span data-stu-id="4f010-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificado EAP \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="4f010-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-118">0x3</span><span class="sxs-lookup"><span data-stu-id="4f010-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="4f010-119">O certificado de usuário expirou.</span><span class="sxs-lookup"><span data-stu-id="4f010-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificado EAP \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="4f010-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-121">0x4</span><span class="sxs-lookup"><span data-stu-id="4f010-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="4f010-122">O certificado de usuário foi revogado.</span><span class="sxs-lookup"><span data-stu-id="4f010-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ outro erro de certificado EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4f010-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-124">0x5</span><span class="sxs-lookup"><span data-stu-id="4f010-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="4f010-125">Há um erro desconhecido relacionado ao certificado.</span><span class="sxs-lookup"><span data-stu-id="4f010-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificado EAP \_ rejeitado**</span><span class="sxs-lookup"><span data-stu-id="4f010-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-127">0x6</span><span class="sxs-lookup"><span data-stu-id="4f010-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="4f010-128">O certificado de usuário foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="4f010-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_nome de certificado EAP \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="4f010-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-130">0x7</span><span class="sxs-lookup"><span data-stu-id="4f010-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="4f010-131">O certificado de usuário requer um nome.</span><span class="sxs-lookup"><span data-stu-id="4f010-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ geral \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="4f010-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-133">0x10</span><span class="sxs-lookup"><span data-stu-id="4f010-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="4f010-134">Define o limite dos relatórios de erros; qualquer erro geral de EAP ocorrerá entre o **\_ EAP \_ geral \_ primeiro** e o **\_ EAP \_ geral, \_ por fim**.</span><span class="sxs-lookup"><span data-stu-id="4f010-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f010-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ geral \_ último**</span><span class="sxs-lookup"><span data-stu-id="4f010-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f010-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="4f010-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="4f010-137">Define o limite dos relatórios de erros; qualquer erro geral de EAP ocorrerá entre o **\_ EAP \_ geral \_ primeiro** e o **\_ EAP \_ geral, \_ por fim**.</span><span class="sxs-lookup"><span data-stu-id="4f010-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f010-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f010-138">Requirements</span></span>



| <span data-ttu-id="4f010-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f010-139">Requirement</span></span> | <span data-ttu-id="4f010-140">Valor</span><span class="sxs-lookup"><span data-stu-id="4f010-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f010-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f010-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4f010-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f010-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4f010-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f010-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4f010-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f010-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4f010-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f010-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f010-146"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f010-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f010-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f010-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f010-148">Constantes do EAPHost comuns</span><span class="sxs-lookup"><span data-stu-id="4f010-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





