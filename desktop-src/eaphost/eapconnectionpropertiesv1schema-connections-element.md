---
title: Elemento Connections
description: Saiba mais sobre o elemento Connections. Esse elemento coleta e contém zero ou mais elementos de conexão.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105815533"
---
# <a name="connections-element"></a><span data-ttu-id="66d27-105">Elemento Connections</span><span class="sxs-lookup"><span data-stu-id="66d27-105">Connections Element</span></span>

<span data-ttu-id="66d27-106">O elemento **Connections** coleta e contém zero ou mais elementos [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66d27-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="66d27-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="66d27-107">Child elements</span></span>



| <span data-ttu-id="66d27-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="66d27-108">Element</span></span>                                                                              | <span data-ttu-id="66d27-109">Type</span><span class="sxs-lookup"><span data-stu-id="66d27-109">Type</span></span>   | <span data-ttu-id="66d27-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="66d27-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66d27-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="66d27-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="66d27-112">Identifica o elemento de configuração EAP.</span><span class="sxs-lookup"><span data-stu-id="66d27-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="66d27-113">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="66d27-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="66d27-114">Define cada definição de configuração e a associa a um nome.</span><span class="sxs-lookup"><span data-stu-id="66d27-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="66d27-115">O elemento [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="66d27-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="66d27-116">**Nome**</span><span class="sxs-lookup"><span data-stu-id="66d27-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="66d27-117">string</span><span class="sxs-lookup"><span data-stu-id="66d27-117">string</span></span> | <span data-ttu-id="66d27-118">Captura o nome da conexão que está sendo definida, auxiliando na identificação de várias conexões.</span><span class="sxs-lookup"><span data-stu-id="66d27-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="66d27-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="66d27-119">Remarks</span></span>

<span data-ttu-id="66d27-120">O elemento **Connections** não é usado com métodos herdados por meio de APIs EAPHost.</span><span class="sxs-lookup"><span data-stu-id="66d27-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d27-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d27-121">Requirements</span></span>



| <span data-ttu-id="66d27-122">Função</span><span class="sxs-lookup"><span data-stu-id="66d27-122">Role</span></span> | <span data-ttu-id="66d27-123">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="66d27-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="66d27-124">Cliente</span><span class="sxs-lookup"><span data-stu-id="66d27-124">Client</span></span><br/> | <span data-ttu-id="66d27-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66d27-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66d27-126">Servidor</span><span class="sxs-lookup"><span data-stu-id="66d27-126">Server</span></span><br/> | <span data-ttu-id="66d27-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66d27-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66d27-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="66d27-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d27-129">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="66d27-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="66d27-130">Esquema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="66d27-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





