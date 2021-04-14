---
description: Uma lista de identificadores de territórios da NAI (identificador de acesso à rede).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Elemento NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502235"
---
# <a name="nairealm-hotspot2-element"></a><span data-ttu-id="cc4f3-103">Elemento NAIRealm (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="cc4f3-103">NAIRealm (Hotspot2) Element</span></span>

<span data-ttu-id="cc4f3-104">Uma lista de identificadores de territórios da NAI (identificador de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="cc4f3-104">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="cc4f3-105">As entradas nessa lista geralmente são do formulário `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="cc4f3-105">Entries in this list are usually of the form `user@domain`.</span></span> <span data-ttu-id="cc4f3-106">A lista de territórios da NAI é o método preferencial para identificar a maioria dos operadores não móveis, como MSOs, operadores de conexão e locais públicos.</span><span class="sxs-lookup"><span data-stu-id="cc4f3-106">The NAI Realm list is the preferred method to identify most non-mobile operators like MSOs, wireline operators, and public venues.</span></span>

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="cc4f3-107">O elemento é definido pelo elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cc4f3-107">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cc4f3-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc4f3-108">Child elements</span></span>



| <span data-ttu-id="cc4f3-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc4f3-109">Element</span></span> | <span data-ttu-id="cc4f3-110">Type</span><span class="sxs-lookup"><span data-stu-id="cc4f3-110">Type</span></span> | <span data-ttu-id="cc4f3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc4f3-111">Description</span></span>                                                   |
|---------|------|---------------------------------------------------------------|
| <span data-ttu-id="cc4f3-112">name</span><span class="sxs-lookup"><span data-stu-id="cc4f3-112">name</span></span>    |      | <span data-ttu-id="cc4f3-113">Um único identificador de realm.</span><span class="sxs-lookup"><span data-stu-id="cc4f3-113">A single realm identifier.</span></span> <span data-ttu-id="cc4f3-114">Geralmente do formulário `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="cc4f3-114">Usually of the form `user@domain`.</span></span> |



 

 



