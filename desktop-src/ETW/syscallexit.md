---
description: Essa classe é a classe de tipo de evento para eventos de saída de chamada do sistema. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Classe SysCallExit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968031"
---
# <a name="syscallexit-class"></a><span data-ttu-id="33189-104">Classe SysCallExit</span><span class="sxs-lookup"><span data-stu-id="33189-104">SysCallExit class</span></span>

<span data-ttu-id="33189-105">Essa classe é a classe de tipo de evento para eventos de saída de chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="33189-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="33189-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="33189-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="33189-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33189-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="33189-108">Membros</span><span class="sxs-lookup"><span data-stu-id="33189-108">Members</span></span>

<span data-ttu-id="33189-109">A classe **SysCallExit** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33189-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="33189-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33189-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33189-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33189-111">Properties</span></span>

<span data-ttu-id="33189-112">A classe **SysCallExit** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="33189-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33189-113">**SysCallNtStatus**</span><span class="sxs-lookup"><span data-stu-id="33189-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33189-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33189-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33189-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33189-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33189-116">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="33189-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="33189-117">Código de status retornado pela chamada do sistema NT.</span><span class="sxs-lookup"><span data-stu-id="33189-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33189-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33189-118">Requirements</span></span>



| <span data-ttu-id="33189-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33189-119">Requirement</span></span> | <span data-ttu-id="33189-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33189-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33189-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33189-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33189-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33189-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33189-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33189-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33189-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33189-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




