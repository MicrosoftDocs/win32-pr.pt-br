---
title: Tipo complexo XmlType
description: Define um fragmento XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Log de eventos do tipo complexo XmlType
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369597"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="85b09-104">Tipo complexo XmlType</span><span class="sxs-lookup"><span data-stu-id="85b09-104">XmlType Complex Type</span></span>

<span data-ttu-id="85b09-105">Define um fragmento XML.</span><span class="sxs-lookup"><span data-stu-id="85b09-105">Defines an XML fragment.</span></span> <span data-ttu-id="85b09-106">Qualquer instância de esquema é permitida; o nó de nível superior no fragmento deve conter um atributo de namespace.</span><span class="sxs-lookup"><span data-stu-id="85b09-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="85b09-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85b09-107">Requirements</span></span>



| <span data-ttu-id="85b09-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b09-108">Requirement</span></span> | <span data-ttu-id="85b09-109">Valor</span><span class="sxs-lookup"><span data-stu-id="85b09-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85b09-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85b09-110">Minimum supported client</span></span><br/> | <span data-ttu-id="85b09-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85b09-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85b09-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85b09-112">Minimum supported server</span></span><br/> | <span data-ttu-id="85b09-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85b09-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





