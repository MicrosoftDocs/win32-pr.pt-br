---
description: Define um tipo de identificador global exclusivo, no formato de registro.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo simples de GUIDtype (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828379"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="5f14f-103">Tipo simples de GUIDtype (contadores de desempenho)</span><span class="sxs-lookup"><span data-stu-id="5f14f-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="5f14f-104">Define um tipo de identificador global exclusivo, no formato de registro.</span><span class="sxs-lookup"><span data-stu-id="5f14f-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5f14f-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="5f14f-105">Patterns</span></span>

<span data-ttu-id="5f14f-106">O tipo simples de **guidtype** é um **xs: String** que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="5f14f-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="5f14f-107">O valor deve ser um tipo de identificador globalmente exclusivo no formato do registro.</span><span class="sxs-lookup"><span data-stu-id="5f14f-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="5f14f-108">Por exemplo, {5b2fc63a-8af4-44cb-960C-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="5f14f-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="5f14f-109">Use GUIDGen.exe ou UUIDGen.exe para criar um GUID.</span><span class="sxs-lookup"><span data-stu-id="5f14f-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f14f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f14f-110">Requirements</span></span>



| <span data-ttu-id="5f14f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f14f-111">Requirement</span></span> | <span data-ttu-id="5f14f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5f14f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f14f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f14f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f14f-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f14f-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f14f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f14f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f14f-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f14f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




