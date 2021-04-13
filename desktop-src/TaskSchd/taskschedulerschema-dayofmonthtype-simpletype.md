---
title: Tipo simples de dayOfMonthType
description: Define os valores possíveis para especificar um dia do mês.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Agendador de Tarefas tipo simples de dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499283"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="54826-104">Tipo simples de dayOfMonthType</span><span class="sxs-lookup"><span data-stu-id="54826-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="54826-105">Define os valores possíveis para especificar um dia do mês.</span><span class="sxs-lookup"><span data-stu-id="54826-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="54826-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="54826-106">Patterns</span></span>

<span data-ttu-id="54826-107">O tipo simples **dayOfMonthType** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="54826-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="54826-108">Especifica o 1º até o dia 31 do mês ou sempre o último dia do mês.</span><span class="sxs-lookup"><span data-stu-id="54826-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="54826-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54826-109">Requirements</span></span>



| <span data-ttu-id="54826-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="54826-110">Requirement</span></span> | <span data-ttu-id="54826-111">Valor</span><span class="sxs-lookup"><span data-stu-id="54826-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54826-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54826-112">Minimum supported client</span></span><br/> | <span data-ttu-id="54826-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54826-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54826-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54826-114">Minimum supported server</span></span><br/> | <span data-ttu-id="54826-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54826-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54826-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="54826-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54826-117">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54826-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="54826-118">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54826-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





