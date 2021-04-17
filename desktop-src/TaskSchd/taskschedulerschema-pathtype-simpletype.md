---
title: Tipo simples PathType
description: Define o número mínimo e máximo de caracteres para uma cadeia de caracteres que define um caminho de arquivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- tipo simples de PathType Agendador de Tarefas
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780105"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="72ca6-104">Tipo simples PathType</span><span class="sxs-lookup"><span data-stu-id="72ca6-104">pathType Simple Type</span></span>

<span data-ttu-id="72ca6-105">Define o número mínimo e máximo de caracteres para uma cadeia de caracteres que define um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="72ca6-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="72ca6-106">O caminho não pode ser uma cadeia de caracteres vazia e deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="72ca6-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="72ca6-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72ca6-107">Requirements</span></span>



| <span data-ttu-id="72ca6-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ca6-108">Requirement</span></span> | <span data-ttu-id="72ca6-109">Valor</span><span class="sxs-lookup"><span data-stu-id="72ca6-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72ca6-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ca6-110">Minimum supported client</span></span><br/> | <span data-ttu-id="72ca6-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72ca6-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72ca6-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ca6-112">Minimum supported server</span></span><br/> | <span data-ttu-id="72ca6-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72ca6-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





