---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica que o EAP-TLS deve ler o certificado do meu repositório do usuário ou do computador que está sendo autenticado.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499559"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="07b03-104">Elemento CertificateStore (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="07b03-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="07b03-105">O elemento **CertificateStore (CredentialsSourceParameters)** indica que o EAP-TLS deve ler o certificado do meu repositório do usuário ou do computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="07b03-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="07b03-106">O elemento **CertificateStore** é definido pelo tipo complexo [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="07b03-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b03-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="07b03-107">Remarks</span></span>

<span data-ttu-id="07b03-108">Os elementos **CertificateStore** e [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="07b03-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="07b03-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b03-109">Requirements</span></span>



| <span data-ttu-id="07b03-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b03-110">Requirement</span></span> | <span data-ttu-id="07b03-111">Valor</span><span class="sxs-lookup"><span data-stu-id="07b03-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07b03-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b03-112">Minimum supported client</span></span><br/> | <span data-ttu-id="07b03-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07b03-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07b03-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b03-114">Minimum supported server</span></span><br/> | <span data-ttu-id="07b03-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07b03-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07b03-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="07b03-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="07b03-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="07b03-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="07b03-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="07b03-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="07b03-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="07b03-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="07b03-120">**CredentialName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="07b03-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="07b03-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="07b03-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="07b03-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="07b03-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="07b03-123">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="07b03-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="07b03-124">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="07b03-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





