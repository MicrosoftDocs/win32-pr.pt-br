---
description: Essa classe é a classe de tipo de evento para eventos de solicitação de conclusão de driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Classe DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967300"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="0954a-104">Classe DriverCompleteRequest</span><span class="sxs-lookup"><span data-stu-id="0954a-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="0954a-105">Essa classe é a classe de tipo de evento para eventos de solicitação de conclusão de driver.</span><span class="sxs-lookup"><span data-stu-id="0954a-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="0954a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0954a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0954a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0954a-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="0954a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0954a-108">Members</span></span>

<span data-ttu-id="0954a-109">A classe **DriverCompleteRequest** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0954a-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="0954a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0954a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0954a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0954a-111">Properties</span></span>

<span data-ttu-id="0954a-112">A classe **DriverCompleteRequest** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0954a-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0954a-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="0954a-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0954a-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0954a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0954a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0954a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0954a-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="0954a-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0954a-117">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="0954a-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="0954a-118">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="0954a-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0954a-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0954a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0954a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0954a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0954a-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="0954a-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0954a-122">Endereço da função de driver que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="0954a-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="0954a-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="0954a-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0954a-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0954a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0954a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0954a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0954a-126">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0954a-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0954a-127">Identificador que identifica a solicitação de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="0954a-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="0954a-128">Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .</span><span class="sxs-lookup"><span data-stu-id="0954a-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0954a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0954a-129">Requirements</span></span>



| <span data-ttu-id="0954a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0954a-130">Requirement</span></span> | <span data-ttu-id="0954a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0954a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0954a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0954a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0954a-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0954a-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0954a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0954a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0954a-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0954a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0954a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0954a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0954a-137">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="0954a-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




