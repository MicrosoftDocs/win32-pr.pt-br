---
title: Tipo simples de strTableRef
description: Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem que é definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Log de eventos de tipo simples strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499448"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="95dd5-104">Tipo simples de strTableRef</span><span class="sxs-lookup"><span data-stu-id="95dd5-104">strTableRef Simple Type</span></span>

<span data-ttu-id="95dd5-105">Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem que é definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (. MC).</span><span class="sxs-lookup"><span data-stu-id="95dd5-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="95dd5-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="95dd5-106">Patterns</span></span>

<span data-ttu-id="95dd5-107">O tipo simples **strTableRef** é um **xs: String** que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="95dd5-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="95dd5-108">A cadeia de caracteres deve estar no formato, $string. *stringid* ou $MC.*symbolid*.</span><span class="sxs-lookup"><span data-stu-id="95dd5-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="95dd5-109">Se a cadeia de caracteres estiver no formato, $string. *stringid*, ele deve fazer referência a uma cadeia de caracteres na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="95dd5-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="95dd5-110">Se a cadeia de caracteres estiver no formato, $mc.*symbolid*, ela deverá fazer referência a um símbolo definido no arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="95dd5-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="95dd5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95dd5-111">Requirements</span></span>



| <span data-ttu-id="95dd5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="95dd5-112">Requirement</span></span> | <span data-ttu-id="95dd5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="95dd5-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="95dd5-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95dd5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="95dd5-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95dd5-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="95dd5-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95dd5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="95dd5-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="95dd5-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





