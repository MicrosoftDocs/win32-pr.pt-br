---
title: Elemento EapHostConfig
description: Contém o elemento EapMethod e o elemento config ou ConfigBlob. Os elementos config e ConfigBlob não podem ser usados simultaneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Elemento EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008790"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="e54d7-105">Elemento EapHostConfig</span><span class="sxs-lookup"><span data-stu-id="e54d7-105">EapHostConfig Element</span></span>

<span data-ttu-id="e54d7-106">O elemento **EapHostConfig** contém o elemento [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) e o elemento [**config**](eaphostconfigschema-config-eaphostconfig-element.md) ou [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e54d7-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="e54d7-107">Os elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e54d7-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="e54d7-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e54d7-108">Child elements</span></span>



| <span data-ttu-id="e54d7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e54d7-109">Element</span></span>                                                                    | <span data-ttu-id="e54d7-110">Type</span><span class="sxs-lookup"><span data-stu-id="e54d7-110">Type</span></span>                                                                                     | <span data-ttu-id="e54d7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e54d7-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e54d7-112">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="e54d7-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="e54d7-113">**BaseEapMethodConfig**</span><span class="sxs-lookup"><span data-stu-id="e54d7-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="e54d7-114">É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.</span><span class="sxs-lookup"><span data-stu-id="e54d7-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="e54d7-115">**ConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="e54d7-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="e54d7-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e54d7-116">hexBinary</span></span>                                                                                | <span data-ttu-id="e54d7-117">É usado quando a configuração do método está em formato de BLOB binário em vez de formulário de texto de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e54d7-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="e54d7-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="e54d7-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="e54d7-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="e54d7-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="e54d7-120">Identifica o método que está sendo referenciado.</span><span class="sxs-lookup"><span data-stu-id="e54d7-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="e54d7-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e54d7-121">Remarks</span></span>

<span data-ttu-id="e54d7-122">O elemento **ProcessContents** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="e54d7-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="e54d7-123">O elemento **ProcessContents** é opcional.</span><span class="sxs-lookup"><span data-stu-id="e54d7-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54d7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e54d7-124">Requirements</span></span>



| <span data-ttu-id="e54d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e54d7-125">Requirement</span></span> | <span data-ttu-id="e54d7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e54d7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e54d7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e54d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e54d7-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e54d7-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e54d7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e54d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e54d7-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e54d7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e54d7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e54d7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54d7-132">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="e54d7-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e54d7-133">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="e54d7-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





