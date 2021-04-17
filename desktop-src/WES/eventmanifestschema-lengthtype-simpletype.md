---
title: Tipo simples de lengthtype
description: Define um tipo de comprimento que é usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LogType de tipo simples de comprimento
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295889"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="c4a81-104">Tipo simples de lengthtype</span><span class="sxs-lookup"><span data-stu-id="c4a81-104">LengthType Simple Type</span></span>

<span data-ttu-id="c4a81-105">Define um tipo de comprimento que é usado para especificar o número de bytes ou caracteres em um item de dados de comprimento variável, como dados binários ou uma cadeia de caracteres ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="c4a81-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="c4a81-106">O valor pode ser especificado como um valor xs: unsignedShort ou como uma cadeia de caracteres que faz referência ao nome do nó de item de dados que contém o valor curto sem sinal.</span><span class="sxs-lookup"><span data-stu-id="c4a81-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="c4a81-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a81-107">Requirements</span></span>



| <span data-ttu-id="c4a81-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a81-108">Requirement</span></span> | <span data-ttu-id="c4a81-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a81-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4a81-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a81-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a81-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4a81-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4a81-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a81-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a81-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4a81-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





