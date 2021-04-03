---
title: Tipo complexo ServerValidationParameters (PEAP)
description: Saiba mais sobre o tipo complexo ServerValidationParameters. Esse tipo contém informações sobre como executar a validação do servidor. | Tipo complexo ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
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
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930284"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="c1b22-106">Tipo complexo ServerValidationParameters (PEAP)</span><span class="sxs-lookup"><span data-stu-id="c1b22-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="c1b22-107">O tipo complexo **ServerValidationParameters** contém informações sobre como executar a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c1b22-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c1b22-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c1b22-108">Child elements</span></span>



| <span data-ttu-id="c1b22-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c1b22-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="c1b22-110">Type</span><span class="sxs-lookup"><span data-stu-id="c1b22-110">Type</span></span>        | <span data-ttu-id="c1b22-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1b22-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b22-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="c1b22-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="c1b22-113">booleano</span><span class="sxs-lookup"><span data-stu-id="c1b22-113">boolean</span></span>     | <span data-ttu-id="c1b22-114">Indica se o usuário deve ser solicitado a fazer a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c1b22-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="c1b22-115">Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) for true, o PEAP executará a validação do servidor sem entrada do usuário; se a validação falhar, o PEAP falhará na autenticação.</span><span class="sxs-lookup"><span data-stu-id="c1b22-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="c1b22-116">Se [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) for false, o usuário será solicitado a fornecer um certificado ou nome de servidor validado ou AC (autoridade de certificação) raiz.</span><span class="sxs-lookup"><span data-stu-id="c1b22-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="c1b22-117">O elemento [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="c1b22-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="c1b22-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="c1b22-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="c1b22-119">complexType</span><span class="sxs-lookup"><span data-stu-id="c1b22-119">complextype</span></span> | <span data-ttu-id="c1b22-120">Representa uma lista de servidores que o cliente confia.</span><span class="sxs-lookup"><span data-stu-id="c1b22-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="c1b22-121">Cada nome de servidor é delimitado por ponto e vírgula e pode ser representado por expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="c1b22-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="c1b22-122">O elemento [**servernames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="c1b22-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c1b22-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="c1b22-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="c1b22-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="c1b22-124">hexBinary</span></span>   | <span data-ttu-id="c1b22-125">Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="c1b22-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="c1b22-126">O Thumb Print é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado</span><span class="sxs-lookup"><span data-stu-id="c1b22-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="c1b22-127">O elemento [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="c1b22-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="c1b22-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1b22-128">Attributes</span></span>



| <span data-ttu-id="c1b22-129">Nome</span><span class="sxs-lookup"><span data-stu-id="c1b22-129">Name</span></span>                    | <span data-ttu-id="c1b22-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1b22-130">Type</span></span>    | <span data-ttu-id="c1b22-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1b22-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b22-132">PerformServerValidation</span><span class="sxs-lookup"><span data-stu-id="c1b22-132">PerformServerValidation</span></span> | <span data-ttu-id="c1b22-133">booleano</span><span class="sxs-lookup"><span data-stu-id="c1b22-133">boolean</span></span> | <span data-ttu-id="c1b22-134">Windows 7 ou posterior: indica se a validação do servidor é executada.</span><span class="sxs-lookup"><span data-stu-id="c1b22-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="c1b22-135">O elemento [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="c1b22-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c1b22-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b22-136">Requirements</span></span>



| <span data-ttu-id="c1b22-137">Função</span><span class="sxs-lookup"><span data-stu-id="c1b22-137">Role</span></span> | <span data-ttu-id="c1b22-138">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b22-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="c1b22-139">Cliente</span><span class="sxs-lookup"><span data-stu-id="c1b22-139">Client</span></span><br/> | <span data-ttu-id="c1b22-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1b22-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1b22-141">Servidor</span><span class="sxs-lookup"><span data-stu-id="c1b22-141">Server</span></span><br/> | <span data-ttu-id="c1b22-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1b22-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1b22-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1b22-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b22-144">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="c1b22-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c1b22-145">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1b22-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c1b22-146">Tipos complexos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1b22-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c1b22-147">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="c1b22-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





