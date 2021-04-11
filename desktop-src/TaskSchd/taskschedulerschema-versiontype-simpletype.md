---
title: Tipo simples versiontype
description: Define um padrão que especifica uma versão de uma tarefa.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- tipo simples de versiontype Agendador de Tarefas
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294781"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="7070c-104">Tipo simples versiontype</span><span class="sxs-lookup"><span data-stu-id="7070c-104">versionType Simple Type</span></span>

<span data-ttu-id="7070c-105">Define um padrão que especifica uma versão de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="7070c-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7070c-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="7070c-106">Patterns</span></span>

<span data-ttu-id="7070c-107">O tipo simples **versiontype** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="7070c-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="7070c-108">Um duplo seguido de um, dois ou três duplos.</span><span class="sxs-lookup"><span data-stu-id="7070c-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="7070c-109">Por exemplo, 1,2 ou 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="7070c-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="7070c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7070c-110">Requirements</span></span>



| <span data-ttu-id="7070c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7070c-111">Requirement</span></span> | <span data-ttu-id="7070c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7070c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7070c-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7070c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7070c-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7070c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7070c-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7070c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7070c-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7070c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





