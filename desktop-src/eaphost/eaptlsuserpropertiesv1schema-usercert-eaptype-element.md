---
title: Elemento usercert (EapType)
description: Refere-se ao hash SHA-1 do certificado que deve ser usado para autenticação.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Elemento usercert EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645074"
---
# <a name="usercert-eaptype-element"></a><span data-ttu-id="a8e01-104">Elemento usercert (EapType)</span><span class="sxs-lookup"><span data-stu-id="a8e01-104">UserCert (EapType) Element</span></span>

<span data-ttu-id="a8e01-105">O elemento **usercert (EapType)** refere-se ao hash SHA-1 do certificado que deve ser usado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="a8e01-105">The **UserCert (EapType)** element refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span>

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

<span data-ttu-id="a8e01-106">O elemento **usercert** é definido pelo elemento [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e01-106">The **UserCert** element is defined by the [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e01-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8e01-107">Requirements</span></span>



| <span data-ttu-id="a8e01-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e01-108">Requirement</span></span> | <span data-ttu-id="a8e01-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a8e01-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8e01-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8e01-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e01-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8e01-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8e01-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8e01-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e01-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8e01-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8e01-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a8e01-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8e01-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a8e01-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8e01-116">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a8e01-116">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="a8e01-117">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a8e01-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8e01-118">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a8e01-118">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="a8e01-119">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="a8e01-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a8e01-120">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a8e01-120">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





