---
title: Elemento SimpleCertSelection (CertSelection)
description: Saiba mais sobre o elemento SimpleCertSelection (CertSelection). Esse elemento determina como o usuário seleciona um certificado.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008377"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="fb03e-105">Elemento SimpleCertSelection (CertSelection)</span><span class="sxs-lookup"><span data-stu-id="fb03e-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="fb03e-106">O elemento **SimpleCertSelection (CertSelection)** determina como o usuário seleciona um certificado.</span><span class="sxs-lookup"><span data-stu-id="fb03e-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="fb03e-107">O elemento **SimpleCertSelection** é definido pelo tipo complexo [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fb03e-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb03e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb03e-108">Remarks</span></span>

<span data-ttu-id="fb03e-109">**SimpleCertSelection** é true por padrão.</span><span class="sxs-lookup"><span data-stu-id="fb03e-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="fb03e-110">Se **SimpleCertSelection** for true, o EAP-TLS executará uma pesquisa de certificado simples sem nenhuma lista suspensa para a seleção de certificados.</span><span class="sxs-lookup"><span data-stu-id="fb03e-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="fb03e-111">Se **SimpleCertSelection** for false, o EAP-TLS ilustrará para o usuário o certificado adequado a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="fb03e-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb03e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb03e-112">Requirements</span></span>



| <span data-ttu-id="fb03e-113">Função</span><span class="sxs-lookup"><span data-stu-id="fb03e-113">Role</span></span> | <span data-ttu-id="fb03e-114">SO com suporte mínimo</span><span class="sxs-lookup"><span data-stu-id="fb03e-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="fb03e-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="fb03e-115">Client</span></span><br/> | <span data-ttu-id="fb03e-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb03e-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb03e-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="fb03e-117">Server</span></span><br/> | <span data-ttu-id="fb03e-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb03e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb03e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb03e-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb03e-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="fb03e-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fb03e-121">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="fb03e-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="fb03e-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="fb03e-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fb03e-123">**CertificateStore (CredentialsSourceParameters)**</span><span class="sxs-lookup"><span data-stu-id="fb03e-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="fb03e-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fb03e-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="fb03e-125">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="fb03e-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fb03e-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb03e-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="fb03e-127">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb03e-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





