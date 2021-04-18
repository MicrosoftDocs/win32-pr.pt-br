---
title: Tipo complexo ServerValidationParameters (TLS)
description: Saiba mais sobre o tipo complexo ServerValidationParameters. Esse tipo contém informações sobre como executar a validação do servidor. | Tipo complexo ServerValidationParameters (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- ServerValidationParameters tipo complexo EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763267"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="d2991-106">Tipo complexo ServerValidationParameters (TLS)</span><span class="sxs-lookup"><span data-stu-id="d2991-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="d2991-107">O tipo complexo **ServerValidationParameters** contém informações sobre como executar a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2991-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d2991-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d2991-108">Child elements</span></span>



| <span data-ttu-id="d2991-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d2991-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="d2991-110">Type</span><span class="sxs-lookup"><span data-stu-id="d2991-110">Type</span></span>      | <span data-ttu-id="d2991-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2991-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2991-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="d2991-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="d2991-113">booleano</span><span class="sxs-lookup"><span data-stu-id="d2991-113">boolean</span></span>   | <span data-ttu-id="d2991-114">Indica se o usuário deve ser solicitado a fazer a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2991-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="d2991-115">Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) for true, o EAP-TLS executará a validação do servidor sem a entrada do usuário; se a validação falhar, o EAP-TLS falhará na autenticação.</span><span class="sxs-lookup"><span data-stu-id="d2991-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="d2991-116">Se [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.</span><span class="sxs-lookup"><span data-stu-id="d2991-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="d2991-117">O elemento [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="d2991-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="d2991-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="d2991-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="d2991-119">string</span><span class="sxs-lookup"><span data-stu-id="d2991-119">string</span></span>    | <span data-ttu-id="d2991-120">Representa uma lista de servidores que o cliente confia.</span><span class="sxs-lookup"><span data-stu-id="d2991-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="d2991-121">Cada nome de servidor é delimitado por ponto e vírgula e pode ser representado por expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="d2991-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="d2991-122">O elemento [**servernames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="d2991-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d2991-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="d2991-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="d2991-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="d2991-124">hexBinary</span></span> | <span data-ttu-id="d2991-125">Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="d2991-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="d2991-126">O Thumb Print é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado</span><span class="sxs-lookup"><span data-stu-id="d2991-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="d2991-127">O elemento [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="d2991-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="d2991-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2991-128">Requirements</span></span>



| <span data-ttu-id="d2991-129">Função</span><span class="sxs-lookup"><span data-stu-id="d2991-129">Role</span></span> | <span data-ttu-id="d2991-130">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="d2991-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d2991-131">Cliente</span><span class="sxs-lookup"><span data-stu-id="d2991-131">Client</span></span><br/> | <span data-ttu-id="d2991-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2991-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2991-133">Servidor</span><span class="sxs-lookup"><span data-stu-id="d2991-133">Server</span></span><br/> | <span data-ttu-id="d2991-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2991-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2991-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2991-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2991-136">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d2991-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d2991-137">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d2991-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d2991-138">Tipos complexos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d2991-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





