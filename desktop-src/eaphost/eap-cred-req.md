---
title: '\_ \_ Req de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ . | \_ \_ Req de credenciais EAP (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105794589"
---
# <a name="eap_cred_req"></a><span data-ttu-id="f6418-105">Req. de \_ credenciais EAP \_</span><span class="sxs-lookup"><span data-stu-id="f6418-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="f6418-106">A **estrutura \_ \_ req. de credenciais EAP** armazena as credenciais de segurança EAP em uma estrutura de matriz de [**\_ campo de entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="f6418-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="f6418-107">**Req. de \_ credenciais EAP \_**</span><span class="sxs-lookup"><span data-stu-id="f6418-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="f6418-108">A estrutura do req. de **\_ credenciais \_ EAP** armazena as credenciais de segurança EAP novas e antigas apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do tipo de [**\_ \_ \_ dados \_ de interface do usuário interativo do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial.</span><span class="sxs-lookup"><span data-stu-id="f6418-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6418-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6418-109">Remarks</span></span>

<span data-ttu-id="f6418-110">A estrutura de **\_ \_ req. de credenciais EAP** é usada para dar suporte ao SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="f6418-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="f6418-111">A estrutura de req. de **\_ credenciais \_ EAP** é idêntica à estrutura [**resp de \_ credenciais \_ de EAP**](eap-cred-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="f6418-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6418-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6418-112">Requirements</span></span>



| <span data-ttu-id="f6418-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6418-113">Requirement</span></span> | <span data-ttu-id="f6418-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f6418-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6418-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6418-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6418-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6418-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6418-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6418-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6418-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6418-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6418-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6418-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6418-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6418-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6418-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6418-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6418-122">Estruturas do suplicante EAPHost</span><span class="sxs-lookup"><span data-stu-id="f6418-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="f6418-123">**\_resp de credenciais EAP \_**</span><span class="sxs-lookup"><span data-stu-id="f6418-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="f6418-124">**Req. de \_ expiração de credenciais EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6418-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="f6418-125">[**\_resp de \_ expiração de credenciais EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6418-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6418-126">**\_dados de \_ interface do usuário interativa EAP \_**</span><span class="sxs-lookup"><span data-stu-id="f6418-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="f6418-127">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="f6418-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

