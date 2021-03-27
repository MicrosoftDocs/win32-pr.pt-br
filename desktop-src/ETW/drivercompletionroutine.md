---
description: Essa classe é a classe de tipo de evento para eventos de rotina de driver completo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Classe DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826873"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="5a8cc-104">Classe DriverCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="5a8cc-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="5a8cc-105">Essa classe é a classe de tipo de evento para eventos de rotina de driver completo.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="5a8cc-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a8cc-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="5a8cc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5a8cc-108">Members</span></span>

<span data-ttu-id="5a8cc-109">A classe **DriverCompletionRoutine** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a8cc-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="5a8cc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a8cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a8cc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a8cc-111">Properties</span></span>

<span data-ttu-id="5a8cc-112">A classe **DriverCompletionRoutine** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a8cc-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a8cc-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a8cc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5a8cc-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5a8cc-117">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="5a8cc-118">**Rotina**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a8cc-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a8cc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5a8cc-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5a8cc-122">Endereço da função de driver que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="5a8cc-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a8cc-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a8cc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a8cc-126">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5a8cc-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5a8cc-127">Identificador que identifica a solicitação de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="5a8cc-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="5a8cc-128">Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8cc-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a8cc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a8cc-129">Requirements</span></span>



| <span data-ttu-id="5a8cc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a8cc-130">Requirement</span></span> | <span data-ttu-id="5a8cc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5a8cc-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a8cc-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a8cc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8cc-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a8cc-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a8cc-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a8cc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8cc-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a8cc-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a8cc-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a8cc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8cc-137">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="5a8cc-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




