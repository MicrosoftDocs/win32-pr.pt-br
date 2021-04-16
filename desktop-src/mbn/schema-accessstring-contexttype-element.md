---
description: Identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento accessstring (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779930"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="545ce-103">Elemento accessstring (contextType)</span><span class="sxs-lookup"><span data-stu-id="545ce-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="545ce-104">O elemento **accessstring (ContextType)** identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="545ce-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="545ce-105">Esse elemento pode ter um comprimento máximo de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="545ce-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="545ce-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="545ce-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="545ce-107">O elemento **accessstring** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="545ce-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="545ce-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="545ce-108">Requirements</span></span>



| <span data-ttu-id="545ce-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="545ce-109">Requirement</span></span> | <span data-ttu-id="545ce-110">Valor</span><span class="sxs-lookup"><span data-stu-id="545ce-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="545ce-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="545ce-111">Minimum supported client</span></span><br/> | <span data-ttu-id="545ce-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="545ce-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="545ce-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="545ce-113">Minimum supported server</span></span><br/> | <span data-ttu-id="545ce-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="545ce-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="545ce-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="545ce-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="545ce-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="545ce-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="545ce-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="545ce-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="545ce-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="545ce-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="545ce-119">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="545ce-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




