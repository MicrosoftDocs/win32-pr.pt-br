---
description: Essa classe é a classe de tipo de evento para os eventos de chamada de função principal do driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Classe DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967298"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="5f5ab-104">Classe DriverMajorFunctionCall</span><span class="sxs-lookup"><span data-stu-id="5f5ab-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="5f5ab-105">Essa classe é a classe de tipo de evento para os eventos de chamada de função principal do driver.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="5f5ab-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f5ab-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="5f5ab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5f5ab-108">Members</span></span>

<span data-ttu-id="5f5ab-109">A classe **DriverMajorFunctionCall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f5ab-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="5f5ab-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f5ab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f5ab-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f5ab-111">Properties</span></span>

<span data-ttu-id="5f5ab-112">A classe **DriverMajorFunctionCall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f5ab-113">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-116">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5f5ab-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-117">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ab-118">**IRP**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-121">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5f5ab-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-122">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ab-123">**MajorFunction**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-126">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="5f5ab-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-127">Código que identifica a função principal que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ab-128">**MinorFunction**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-131">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="5f5ab-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-132">Código que idenitifies a função secundária que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ab-133">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-136">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5f5ab-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-137">Endereço da função de driver que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ab-138">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ab-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ab-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ab-141">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="5f5ab-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5f5ab-142">Identificador que identifica a solicitação de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="5f5ab-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="5f5ab-143">Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="5f5ab-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f5ab-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f5ab-144">Requirements</span></span>



| <span data-ttu-id="5f5ab-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5ab-145">Requirement</span></span> | <span data-ttu-id="5f5ab-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5f5ab-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f5ab-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f5ab-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5ab-148">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f5ab-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f5ab-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f5ab-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5ab-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f5ab-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f5ab-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f5ab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5ab-152">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="5f5ab-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




