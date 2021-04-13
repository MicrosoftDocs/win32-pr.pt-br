---
description: Uma representação de cadeia de caracteres de um GUID, no formato usual.
MS-HAID: WWAN\_profile\_v4.simpleType\_guidType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: tipo simples de guidtype (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b7cc19207ab334694e4b42a49f727070cb385d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501643"
---
# <a name="span-idwwan_profile_v4simpletype_guidtypespanguidtype-simple-type-mobile-broadband"></a><span data-ttu-id="0765d-103"><span id="WWAN_profile_v4.simpleType_guidType"></span>tipo simples de guidtype (banda larga móvel)</span><span class="sxs-lookup"><span data-stu-id="0765d-103"><span id="WWAN_profile_v4.simpleType_guidType"></span>guidType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="0765d-104">Uma representação de cadeia de caracteres de um GUID, no formato usual.</span><span class="sxs-lookup"><span data-stu-id="0765d-104">A string representation of a GUID, in the usual format.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="0765d-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="0765d-105">Patterns</span></span>

<span data-ttu-id="0765d-106">O tipo simples **guidtype** é um token que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="0765d-106">The **guidType** simple type is a token that is restricted by the following pattern:</span></span>

-   `{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}`

 

 



