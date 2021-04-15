---
title: Elemento DisableUserPromptForServerValidation (PEAP)
description: Saiba mais sobre o elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se o usuário deve ser solicitado a fazer a validação do servidor. | Elemento DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- Elemento DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105747431"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="cf23b-106">Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="cf23b-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="cf23b-107">O elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se o usuário deve ser solicitado para a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="cf23b-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="cf23b-108">Se **DisableUserPromptForServerValidation** for true, o EAP-TLS executará a validação do servidor sem a entrada do usuário; se a validação falhar, o EAP-TLS falhará na autenticação.</span><span class="sxs-lookup"><span data-stu-id="cf23b-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="cf23b-109">Se **DisableUserPromptForServerValidation** for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.</span><span class="sxs-lookup"><span data-stu-id="cf23b-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="cf23b-110">O elemento **DisableUserPromptForServerValidation** é opcional.</span><span class="sxs-lookup"><span data-stu-id="cf23b-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="cf23b-111">O elemento **DisableUserPromptForServerValidation** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cf23b-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf23b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf23b-112">Requirements</span></span>



| <span data-ttu-id="cf23b-113">Função</span><span class="sxs-lookup"><span data-stu-id="cf23b-113">Role</span></span> | <span data-ttu-id="cf23b-114">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="cf23b-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="cf23b-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="cf23b-115">Client</span></span><br/> | <span data-ttu-id="cf23b-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf23b-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf23b-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="cf23b-117">Server</span></span><br/> | <span data-ttu-id="cf23b-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf23b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf23b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf23b-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf23b-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="cf23b-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cf23b-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="cf23b-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="cf23b-122">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf23b-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cf23b-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="cf23b-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="cf23b-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="cf23b-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="cf23b-125">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="cf23b-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cf23b-126">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cf23b-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="cf23b-127">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cf23b-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





