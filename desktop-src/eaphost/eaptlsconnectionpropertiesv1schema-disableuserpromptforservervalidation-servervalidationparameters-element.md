---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: Saiba mais sobre o elemento DisableUserPromptForServerValidation (ServerValidationParameters). Indica se o usuário deve ser solicitado a fazer a validação do servidor. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
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
ms.openlocfilehash: 368b2593b3c55ef571e3f1892634318e54447643
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172696"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a><span data-ttu-id="60fb3-106">Elemento DisableUserPromptForServerValidation (ServerValidationParameters) (TLS)</span><span class="sxs-lookup"><span data-stu-id="60fb3-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="60fb3-107">O elemento **DisableUserPromptForServerValidation (ServerValidationParameters)** indica se o usuário deve ser solicitado para a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="60fb3-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="60fb3-108">Se **DisableUserPromptForServerValidation** for true, o EAP-TLS executará a validação do servidor sem a entrada do usuário; se a validação falhar, o EAP-TLS falhará na autenticação.</span><span class="sxs-lookup"><span data-stu-id="60fb3-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="60fb3-109">Se **DisableUserPromptForServerValidation** for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.</span><span class="sxs-lookup"><span data-stu-id="60fb3-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="60fb3-110">O elemento **DisableUserPromptForServerValidation** é opcional.</span><span class="sxs-lookup"><span data-stu-id="60fb3-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="60fb3-111">O elemento **DisableUserPromptForServerValidation** é definido pelo tipo complexo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="60fb3-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fb3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60fb3-112">Requirements</span></span>



| <span data-ttu-id="60fb3-113">Função</span><span class="sxs-lookup"><span data-stu-id="60fb3-113">Role</span></span> | <span data-ttu-id="60fb3-114">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="60fb3-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="60fb3-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="60fb3-115">Client</span></span><br/> | <span data-ttu-id="60fb3-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60fb3-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60fb3-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="60fb3-117">Server</span></span><br/> | <span data-ttu-id="60fb3-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60fb3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60fb3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="60fb3-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="60fb3-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="60fb3-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="60fb3-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="60fb3-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="60fb3-122">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="60fb3-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="60fb3-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="60fb3-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="60fb3-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="60fb3-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="60fb3-125">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="60fb3-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="60fb3-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="60fb3-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="60fb3-127">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="60fb3-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





