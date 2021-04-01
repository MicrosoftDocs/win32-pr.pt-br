---
description: Define um nome de símbolo do C/C++ válido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simples de CSymbolType (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921735"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="78931-103">Tipo simples de CSymbolType (contadores de desempenho)</span><span class="sxs-lookup"><span data-stu-id="78931-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="78931-104">Define um nome de símbolo do C/C++ válido.</span><span class="sxs-lookup"><span data-stu-id="78931-104">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="78931-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="78931-105">Patterns</span></span>

<span data-ttu-id="78931-106">O tipo simples **CSymbolType** é um **xs: String** que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="78931-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="78931-107">O nome do símbolo pode ser vazio ou conter caracteres alfanuméricos e sublinhados.</span><span class="sxs-lookup"><span data-stu-id="78931-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="78931-108">Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.</span><span class="sxs-lookup"><span data-stu-id="78931-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="78931-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78931-109">Requirements</span></span>



| <span data-ttu-id="78931-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="78931-110">Requirement</span></span> | <span data-ttu-id="78931-111">Valor</span><span class="sxs-lookup"><span data-stu-id="78931-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78931-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78931-112">Minimum supported client</span></span><br/> | <span data-ttu-id="78931-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78931-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78931-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78931-114">Minimum supported server</span></span><br/> | <span data-ttu-id="78931-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78931-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




