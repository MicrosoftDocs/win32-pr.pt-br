---
description: Essa classe é a classe de tipo de evento para eventos de chamada do sistema Enter. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Classe SysCallEnter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968032"
---
# <a name="syscallenter-class"></a><span data-ttu-id="116e0-104">Classe SysCallEnter</span><span class="sxs-lookup"><span data-stu-id="116e0-104">SysCallEnter class</span></span>

<span data-ttu-id="116e0-105">Essa classe é a classe de tipo de evento para eventos de chamada do sistema Enter.</span><span class="sxs-lookup"><span data-stu-id="116e0-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="116e0-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="116e0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="116e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="116e0-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="116e0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="116e0-108">Members</span></span>

<span data-ttu-id="116e0-109">A classe **SysCallEnter** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="116e0-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="116e0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="116e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="116e0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="116e0-111">Properties</span></span>

<span data-ttu-id="116e0-112">A classe **SysCallEnter** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="116e0-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="116e0-113">**SysCallAddress**</span><span class="sxs-lookup"><span data-stu-id="116e0-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="116e0-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="116e0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="116e0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="116e0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="116e0-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="116e0-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="116e0-117">Endereço da chamada de função NT que está sendo inserida.</span><span class="sxs-lookup"><span data-stu-id="116e0-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="116e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116e0-118">Requirements</span></span>



| <span data-ttu-id="116e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="116e0-119">Requirement</span></span> | <span data-ttu-id="116e0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="116e0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="116e0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="116e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="116e0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="116e0-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="116e0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="116e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="116e0-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="116e0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




