---
title: Tipo complexo CredentialsSourceParameters
description: Define o elemento necessário para especificar a origem do certificado a ser usado com uma autenticação EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters tipo complexo EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085952"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="89e85-104">Tipo complexo CredentialsSourceParameters</span><span class="sxs-lookup"><span data-stu-id="89e85-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="89e85-105">O tipo complexo **CredentialsSourceParameters** define o elemento necessário para especificar a origem do certificado a ser usado com uma autenticação EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="89e85-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="89e85-106">Há uma opção entre o elemento [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ou o elemento [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="89e85-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="89e85-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="89e85-107">Child elements</span></span>



| <span data-ttu-id="89e85-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="89e85-108">Element</span></span>                                                                                                             | <span data-ttu-id="89e85-109">Type</span><span class="sxs-lookup"><span data-stu-id="89e85-109">Type</span></span>                                                                                  | <span data-ttu-id="89e85-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="89e85-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89e85-111">**CertificateStore**</span><span class="sxs-lookup"><span data-stu-id="89e85-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="89e85-112">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="89e85-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="89e85-113">Indica que o EAP-TLS deve ler o certificado do meu repositório do usuário ou do computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="89e85-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="89e85-114">**Smart**</span><span class="sxs-lookup"><span data-stu-id="89e85-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="89e85-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="89e85-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="89e85-116">Indica que o EAP-TLS deve ler o certificado do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="89e85-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="89e85-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89e85-117">Remarks</span></span>

<span data-ttu-id="89e85-118">Os elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="89e85-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e85-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e85-119">Requirements</span></span>



| <span data-ttu-id="89e85-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e85-120">Requirement</span></span> | <span data-ttu-id="89e85-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89e85-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89e85-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e85-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89e85-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89e85-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="89e85-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e85-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89e85-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89e85-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89e85-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="89e85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e85-127">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="89e85-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="89e85-128">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="89e85-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="89e85-129">Tipos complexos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="89e85-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





