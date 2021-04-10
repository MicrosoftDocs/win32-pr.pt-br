---
title: Tipo complexo CertSelection
description: Saiba mais sobre o tipo complexo CertSelection. Esse tipo determina como o usuário seleciona um certificado.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection tipo complexo EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294506"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="92c02-105">Tipo complexo CertSelection</span><span class="sxs-lookup"><span data-stu-id="92c02-105">CertSelection Complex Type</span></span>

<span data-ttu-id="92c02-106">O tipo complexo **CertSelection** determina como o usuário seleciona um certificado.</span><span class="sxs-lookup"><span data-stu-id="92c02-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="92c02-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="92c02-107">Child elements</span></span>



| <span data-ttu-id="92c02-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="92c02-108">Element</span></span>                                                                                                     | <span data-ttu-id="92c02-109">Type</span><span class="sxs-lookup"><span data-stu-id="92c02-109">Type</span></span>    | <span data-ttu-id="92c02-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="92c02-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92c02-111">**SimpleCertSelection**</span><span class="sxs-lookup"><span data-stu-id="92c02-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="92c02-112">booleano</span><span class="sxs-lookup"><span data-stu-id="92c02-112">boolean</span></span> | <span data-ttu-id="92c02-113">É TRUE por padrão.</span><span class="sxs-lookup"><span data-stu-id="92c02-113">Is TRUE by default.</span></span> <span data-ttu-id="92c02-114">Se [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) for true, o EAP-TLS executará uma pesquisa de certificado simples sem nenhuma lista suspensa para a seleção de certificados.</span><span class="sxs-lookup"><span data-stu-id="92c02-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="92c02-115">Se **SimpleCertSelection** for false, o EAP-TLS ilustrará para o usuário o certificado adequado a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="92c02-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="92c02-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c02-116">Requirements</span></span>



| <span data-ttu-id="92c02-117">Função</span><span class="sxs-lookup"><span data-stu-id="92c02-117">Role</span></span> | <span data-ttu-id="92c02-118">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="92c02-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="92c02-119">Cliente</span><span class="sxs-lookup"><span data-stu-id="92c02-119">Client</span></span><br/> | <span data-ttu-id="92c02-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92c02-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92c02-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="92c02-121">Server</span></span><br/> | <span data-ttu-id="92c02-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92c02-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92c02-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c02-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c02-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="92c02-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="92c02-125">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="92c02-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="92c02-126">Tipos complexos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="92c02-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





