---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (esquema de descrição da propriedade)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750882"
---
# <a name="image"></a><span data-ttu-id="78292-103">image</span><span class="sxs-lookup"><span data-stu-id="78292-103">image</span></span>

<span data-ttu-id="78292-104">Deve haver apenas um elemento [Image]() para cada elemento pai.</span><span class="sxs-lookup"><span data-stu-id="78292-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="78292-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78292-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="78292-106">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="78292-106">Element Information</span></span>



| <span data-ttu-id="78292-107">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="78292-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="78292-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="78292-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="78292-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="78292-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="78292-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="78292-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="78292-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="78292-111">Attributes</span></span>



| <span data-ttu-id="78292-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="78292-112">Attribute</span></span> | <span data-ttu-id="78292-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="78292-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="78292-114">res</span><span class="sxs-lookup"><span data-stu-id="78292-114">res</span></span>       | <span data-ttu-id="78292-115">Público.</span><span class="sxs-lookup"><span data-stu-id="78292-115">Public.</span></span> <span data-ttu-id="78292-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="78292-116">Required.</span></span> |



 

 

 
