---
title: '\_ \_ \_ Req de logon de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009136"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="42bb6-104">Req. de \_ logon de credenciais EAP \_ \_</span><span class="sxs-lookup"><span data-stu-id="42bb6-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="42bb6-105">A estrutura do **\_ \_ \_ req logon** de credenciais EAP armazena as credenciais de segurança EAP em uma estrutura de matriz de campo de entrada de [**\_ configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="42bb6-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="42bb6-106">**Req. de \_ logon de credenciais EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42bb6-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="42bb6-107">A **estrutura \_ \_ \_ req logon** de credenciais EAP armazena as credenciais de segurança EAP apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do tipo de [**\_ \_ \_ dados \_ de interface do usuário interativo do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial.</span><span class="sxs-lookup"><span data-stu-id="42bb6-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="42bb6-108">Os campos de entrada nessa estrutura são os mesmos que os campos de entrada retornados por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="42bb6-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="42bb6-109">**EAP \_ O \_ \_ req logon de credenciais** é usado na solicitação de credenciais inicial e o [**\_ \_ req de credenciais EAP**](eap-cred-req.md) é usado na solicitação de repetição de credencial durante uma autenticação.</span><span class="sxs-lookup"><span data-stu-id="42bb6-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42bb6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="42bb6-110">Remarks</span></span>

<span data-ttu-id="42bb6-111">A **estrutura \_ \_ \_ req logon de credenciais EAP** é usada para dar suporte ao SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="42bb6-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="42bb6-112">A **estrutura \_ \_ \_ req logon de credenciais EAP** é idêntica à estrutura [**\_ \_ \_ resp de logon de credenciais EAP**](eap-cred-logon-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="42bb6-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="42bb6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42bb6-113">Requirements</span></span>



| <span data-ttu-id="42bb6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42bb6-114">Requirement</span></span> | <span data-ttu-id="42bb6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="42bb6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42bb6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42bb6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42bb6-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42bb6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42bb6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42bb6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42bb6-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="42bb6-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42bb6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42bb6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42bb6-121"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="42bb6-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42bb6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="42bb6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bb6-123">**\_matriz de \_ campo de entrada de configuração EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42bb6-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="42bb6-124">**Req. de \_ credenciais EAP \_**</span><span class="sxs-lookup"><span data-stu-id="42bb6-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="42bb6-125">**\_dados de \_ interface do usuário interativa EAP \_**</span><span class="sxs-lookup"><span data-stu-id="42bb6-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="42bb6-126">**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42bb6-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="42bb6-127">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="42bb6-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





