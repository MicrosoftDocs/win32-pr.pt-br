---
description: Uma lista de IDs de rede móvel pública (PLMN).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Elemento Network3GPP (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760231"
---
# <a name="network3gpp-hotspot2-element"></a><span data-ttu-id="f1d70-103">Elemento Network3GPP (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="f1d70-103">Network3GPP (Hotspot2) Element</span></span>

<span data-ttu-id="f1d70-104">Uma lista de IDs de rede móvel pública (PLMN).</span><span class="sxs-lookup"><span data-stu-id="f1d70-104">A list of Public Land Mobile Network (PLMN) IDs.</span></span>

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f1d70-105">O elemento é definido pelo elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d70-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f1d70-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f1d70-106">Child elements</span></span>



| <span data-ttu-id="f1d70-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f1d70-107">Element</span></span> | <span data-ttu-id="f1d70-108">Type</span><span class="sxs-lookup"><span data-stu-id="f1d70-108">Type</span></span> | <span data-ttu-id="f1d70-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1d70-109">Description</span></span>                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d70-110">PLMNID</span><span class="sxs-lookup"><span data-stu-id="f1d70-110">PLMNID</span></span>  |      | <span data-ttu-id="f1d70-111">Uma ID de PLMN individual.</span><span class="sxs-lookup"><span data-stu-id="f1d70-111">An individual PLMN ID.</span></span> <span data-ttu-id="f1d70-112">Este é um número decimal de 5 ou 6 dígitos correspondente ao MCC/MNC de uma rede 3GPP.</span><span class="sxs-lookup"><span data-stu-id="f1d70-112">This is a 5 or 6 digit decimal number corresponding to the MCC/MNC of a 3GPP network.</span></span><br/> |



 

 




