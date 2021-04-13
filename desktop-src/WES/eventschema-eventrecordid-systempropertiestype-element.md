---
title: Elemento EventRecordID (SystemPropertiesType)
description: O número de registro atribuído ao evento quando ele foi registrado.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- EventLog do elemento EventRecordID
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369291"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="4a8c5-104">Elemento EventRecordID (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="4a8c5-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="4a8c5-105">O número de registro atribuído ao evento quando ele foi registrado.</span><span class="sxs-lookup"><span data-stu-id="4a8c5-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4a8c5-106">O elemento **EventRecordID** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a8c5-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8c5-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a8c5-107">Requirements</span></span>



| <span data-ttu-id="4a8c5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a8c5-108">Requirement</span></span> | <span data-ttu-id="4a8c5-109">Valor</span><span class="sxs-lookup"><span data-stu-id="4a8c5-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a8c5-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a8c5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8c5-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a8c5-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a8c5-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a8c5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8c5-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a8c5-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





