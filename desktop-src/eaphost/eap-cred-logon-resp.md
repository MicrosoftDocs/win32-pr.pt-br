---
title: '\_ \_ \_ Resp de logon de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ . | \_ \_ \_ Resp de logon de credenciais EAP (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763450"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="65d9b-105">\_resp de \_ logon de credenciais EAP \_</span><span class="sxs-lookup"><span data-stu-id="65d9b-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="65d9b-106">A **estrutura \_ \_ \_ resp de logon de credenciais EAP** armazena as credenciais de segurança EAP em uma estrutura de [**\_ \_ \_ \_ matriz de campo de entrada de configuração EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="65d9b-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="65d9b-107">**\_resp de \_ logon de credenciais EAP \_**</span><span class="sxs-lookup"><span data-stu-id="65d9b-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="65d9b-108">A **estrutura \_ \_ \_ resp de logon de credenciais do EAP** armazena as credenciais de segurança EAP apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do [**tipo de \_ \_ \_ dados \_ da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial.</span><span class="sxs-lookup"><span data-stu-id="65d9b-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="65d9b-109">Os campos de entrada nessa estrutura serão os mesmos dos campos de entrada retornados por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="65d9b-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="65d9b-110">**EAP \_ O \_ logon \_ de credenciais resp** é usado na solicitação de credencial inicial e o [**\_ \_ resp de credenciais de EAP**](eap-cred-resp.md) é usado na solicitação de repetição de credencial durante uma autenticação.</span><span class="sxs-lookup"><span data-stu-id="65d9b-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65d9b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="65d9b-111">Remarks</span></span>

<span data-ttu-id="65d9b-112">A **estrutura \_ \_ \_ resp de logon de credenciais EAP** é usada para dar suporte ao SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="65d9b-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="65d9b-113">A estrutura de **\_ resp de \_ logon \_ de credenciais EAP** é idêntica à estrutura [**\_ \_ \_ req logon de credenciais EAP**](eap-cred-logon-req.md) .</span><span class="sxs-lookup"><span data-stu-id="65d9b-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d9b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d9b-114">Requirements</span></span>



| <span data-ttu-id="65d9b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d9b-115">Requirement</span></span> | <span data-ttu-id="65d9b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="65d9b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65d9b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d9b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65d9b-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65d9b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65d9b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d9b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65d9b-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="65d9b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65d9b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65d9b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="65d9b-122"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d9b-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d9b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="65d9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d9b-124">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="65d9b-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="65d9b-125">**\_matriz de \_ campo de entrada de configuração EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65d9b-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="65d9b-126">**Req. de \_ logon de credenciais EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65d9b-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="65d9b-127">**\_dados de \_ interface do usuário interativa EAP \_**</span><span class="sxs-lookup"><span data-stu-id="65d9b-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="65d9b-128">**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65d9b-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





