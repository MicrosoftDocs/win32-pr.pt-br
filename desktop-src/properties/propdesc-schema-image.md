---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (esquema de descrição da propriedade)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104984"
---
# <a name="image"></a><span data-ttu-id="0cb7c-103">image</span><span class="sxs-lookup"><span data-stu-id="0cb7c-103">image</span></span>

<span data-ttu-id="0cb7c-104">Deve haver apenas um elemento [Image]() para cada elemento pai.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb7c-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0cb7c-106">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0cb7c-106">Element Information</span></span>



| <span data-ttu-id="0cb7c-107">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0cb7c-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="0cb7c-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0cb7c-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="0cb7c-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="0cb7c-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="0cb7c-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0cb7c-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0cb7c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cb7c-111">Attributes</span></span>



| <span data-ttu-id="0cb7c-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="0cb7c-112">Attribute</span></span> | <span data-ttu-id="0cb7c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cb7c-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="0cb7c-114">res</span><span class="sxs-lookup"><span data-stu-id="0cb7c-114">res</span></span>       | <span data-ttu-id="0cb7c-115">Público.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-115">Public.</span></span> <span data-ttu-id="0cb7c-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0cb7c-116">Required.</span></span> |



 

 

 
