---
title: Tipo complexo UserDataType
description: Define um fragmento XML que especifica o layout dos dados do evento.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Log de eventos do tipo complexo UserDataType
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811366"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="dc8d6-104">Tipo complexo UserDataType</span><span class="sxs-lookup"><span data-stu-id="dc8d6-104">UserDataType Complex Type</span></span>

<span data-ttu-id="dc8d6-105">Define um fragmento XML que especifica o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="dc8d6-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="dc8d6-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc8d6-106">Requirements</span></span>



| <span data-ttu-id="dc8d6-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc8d6-107">Requirement</span></span> | <span data-ttu-id="dc8d6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dc8d6-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc8d6-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc8d6-109">Minimum supported client</span></span><br/> | <span data-ttu-id="dc8d6-110">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc8d6-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc8d6-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc8d6-111">Minimum supported server</span></span><br/> | <span data-ttu-id="dc8d6-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc8d6-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





