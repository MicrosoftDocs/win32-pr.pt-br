---
title: Elemento Connection (Connections)
description: Define cada definição de configuração e a associa a um nome. O elemento Connection é opcional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento Connection EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764232"
---
# <a name="connection-connections-element"></a><span data-ttu-id="f6b50-105">Elemento Connection (Connections)</span><span class="sxs-lookup"><span data-stu-id="f6b50-105">Connection (Connections) Element</span></span>

<span data-ttu-id="f6b50-106">O elemento **Connection (Connections)** define cada definição de configuração e a associa a um nome.</span><span class="sxs-lookup"><span data-stu-id="f6b50-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="f6b50-107">O elemento **Connection** é opcional.</span><span class="sxs-lookup"><span data-stu-id="f6b50-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f6b50-108">O elemento **Connection** é definido pelo elemento [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f6b50-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f6b50-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f6b50-109">Child elements</span></span>



| <span data-ttu-id="f6b50-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6b50-110">Element</span></span>                                                                 | <span data-ttu-id="f6b50-111">Type</span><span class="sxs-lookup"><span data-stu-id="f6b50-111">Type</span></span>   | <span data-ttu-id="f6b50-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6b50-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6b50-113">**EAP**</span><span class="sxs-lookup"><span data-stu-id="f6b50-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="f6b50-114">Identifica o elemento de configuração EAP.</span><span class="sxs-lookup"><span data-stu-id="f6b50-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="f6b50-115">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f6b50-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="f6b50-116">string</span><span class="sxs-lookup"><span data-stu-id="f6b50-116">string</span></span> | <span data-ttu-id="f6b50-117">Captura o nome da conexão que está sendo definida, auxiliando na identificação de várias conexões.</span><span class="sxs-lookup"><span data-stu-id="f6b50-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="f6b50-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b50-118">Requirements</span></span>



| <span data-ttu-id="f6b50-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b50-119">Requirement</span></span> | <span data-ttu-id="f6b50-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6b50-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6b50-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6b50-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b50-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6b50-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6b50-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6b50-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b50-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6b50-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6b50-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6b50-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6b50-126">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f6b50-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b50-127">**Conexões**</span><span class="sxs-lookup"><span data-stu-id="f6b50-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="f6b50-128">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f6b50-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b50-129">**Conexões**</span><span class="sxs-lookup"><span data-stu-id="f6b50-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="f6b50-130">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f6b50-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f6b50-131">Esquema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f6b50-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





