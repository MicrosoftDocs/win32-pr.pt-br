---
title: Elemento SmartCard (CredentialsSourceParameters)
description: Indica que o EAP-TLS deve ler o certificado do cartão inteligente.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Elemento SmartCard EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790364"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="f2bc5-104">Elemento SmartCard (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="f2bc5-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="f2bc5-105">O elemento **SmartCard (CredentialsSourceParameters)** indica que o EAP-TLS deve ler o certificado do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="f2bc5-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="f2bc5-106">O elemento **SmartCard** é definido pelo tipo complexo [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2bc5-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bc5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2bc5-107">Remarks</span></span>

<span data-ttu-id="f2bc5-108">Os elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e **SmartCard** não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f2bc5-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bc5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2bc5-109">Requirements</span></span>



| <span data-ttu-id="f2bc5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bc5-110">Requirement</span></span> | <span data-ttu-id="f2bc5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f2bc5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2bc5-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bc5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bc5-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2bc5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2bc5-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bc5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bc5-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2bc5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2bc5-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2bc5-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2bc5-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f2bc5-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f2bc5-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="f2bc5-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="f2bc5-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f2bc5-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f2bc5-120">**CredentialName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="f2bc5-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="f2bc5-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f2bc5-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f2bc5-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f2bc5-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f2bc5-123">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f2bc5-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f2bc5-124">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f2bc5-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





